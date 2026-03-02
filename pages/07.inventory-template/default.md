---
title: 'KNEL — Inventory Template (STEP0)'
menu: 'KNEL — Inventory Template (STEP0)'
---

# KNEL — Inventory Template (STEP0)

CSV headers (example)

```
app_id,app_name,biz,env,slo,cost_center,url,notes
12345,gitea,merchants-of-hope,prod,tier-2,KNEL:GIT-ORG,https://gitea.example.com/org/...,primary code hosting
12346,matomo,your-dream-name-here,prod,tier-2,KNEL:MAT-PROP,https://matomo.example.com/#idSite=...,analytics
12347,documenso,sol-calc,prod,tier-2,KNEL:DOC-SEAT,https://sign.example.com,contracts
12348,redmine,rackrental,prod,tier-3,KNEL:RED-PROJ,https://pm.example.com,project tracking
```

Notes
- Export nightly (CSV/JSON) from Cloudron inventory or maintain manually to start.
- Tags: `biz`, `env`, `slo`, `cost_center` support lightweight reconciliation to Dolibarr.
