# eurofxref
Euro foreign exchange reference rates.

Get the URL below from [Euro foreign exchange reference rates](https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/index.en.html)
```
URL="https://www.ecb.europa.eu/stats/eurofxref/eurofxref-hist.zip?44449512bdd071c13b3990854cd7e2e5"
wget -qO /tmp/eurofxref.zip "${URL}" && unzip /tmp/eurofxref.zip
```

In your Google Sheet import data like this:
```
=QUERY(IMPORTDATA("https://raw.githubusercontent.com/h0tbird/eurofxref/refs/heads/main/eurofxref-hist.csv"), "SELECT Col1, Col2 LABEL Col1 'Date', Col2 'USD'")
```
