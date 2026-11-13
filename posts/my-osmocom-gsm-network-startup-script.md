---
title: My osmocom GSM network startup script
date: 2026-11-13
description: ''
---

#!/bin/bash

echo "Starting GSM..."
systemctl restart osmo-nid
systemctl is-active --quiet asterisk || systemctl start asterisk
for i in $(seq 1 60); do
  pgrep -x osmo-bts-trx >/dev/null && break
  sleep 1
done
sleep 5
echo
if pgrep -x osmo-bts-trx >/dev/null; then
  echo "GSM is up."
else
  echo "The BTS did not start. Check: journalctl -u osmo-nid -e"
fi
ps -eo pid,cmd | grep -E "osmo-(trx|bts|bsc|msc|hlr)" | grep -v grep
