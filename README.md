# ⚡ Daily Systems Operations Log — Karthik Patha  

**Position:** MHE Support Analyst | Burlington Coat Factory  
**Domain:** WMS Integration • Real-Time Automation • System Stability  

---

### 📅 Date: Oct-29-2025 

---

### 🏗️ System Focus of the Day  
🎯 **Objective:** Maintain end-to-end synchronization between **Manhattan WMOS** and **Dematic WCS** to prevent message latency and throughput drops.  
🔍 **Environment:** Production (California DC)  
🧩 **System Components:** Conveyor Routing, Carton Close, Tote Tracking, API Monitoring  

---

### 🧰 Key Activities & Outcomes  

| Activity | Description | Outcome |
|-----------|-------------|----------|
| 🔄 **Message Flow Validation** | Verified inbound/outbound message states (6120–6380) for tote movement and order routing | No message loss detected; improved validation speed by 20% |
| 🧠 **Root Cause Analysis** | Investigated delayed replenishment confirmation messages | Found host table lock on `WCS_Container_Status`; cleared via SQL job |
| ⚙️ **Performance Monitoring** | Used DVF and Postman for API status tracking | Reduced average response delay from 2.3s → 1.6s |
| 📈 **Data Visualization** | Updated Power BI dashboard with daily DC throughput & downtime stats | Highlighted 8% improvement in pick efficiency |
| 🤝 **Cross-Team Collaboration** | Worked with mechanical & ops team on sorter performance checks | Reduced unscheduled downtime incidents |

---

### ⚡ Observations & Insights  

- Message retry frequency in **DVF queue** increased during batch closure — scheduled a test for tomorrow to adjust intervals.  
- SQL audit query revealed **4 duplicate routing events**, which caused minor delay in pallet confirmation.  
- Improved alert granularity in **Power BI SLA Dashboard** by adding real-time refresh trigger.  

---

### 🧠 Today’s Learning  
> Learned how **Manhattan WMOS routing logic** interacts with **Dematic handshake acknowledgment** during carton reallocation.  
> Also experimented with **SQL window functions** to
