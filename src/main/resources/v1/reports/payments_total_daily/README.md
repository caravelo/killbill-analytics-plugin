# Daily payments report

Compute the total value (in the reference currency) of captured payments per day per currency.

The snapshot view is: `v_report_payments_total_daily`

## Timeline configuration

```
curl -v \
     -X POST \
     -u admin:password \
     -H "X-Killbill-ApiKey:bob" \
     -H "X-Killbill-ApiSecret:lazar" \
     -H 'Content-Type: application/json' \
     -d '{"reportName": "report_payments_total_daily",
          "reportType": "TIMELINE",
          "reportPrettyName": "Daily payments value",
          "sourceTableName": "report_payments_total_daily",
          "refreshProcedureName": "refresh_report_payments_total_daily",
          "refreshFrequency": "HOURLY"}' \
     "http://127.0.0.1:8080/plugins/killbill-analytics/reports"
```
