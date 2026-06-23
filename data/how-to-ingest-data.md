# How Data Is Ingested into Dynatrace (Easy Explanation)

Before Dynatrace can analyze logs, detect anomalies, or identify root causes, it must first receive data from the systems being monitored. This process is called **Data Ingestion**.

The overall workflow is simple:

```text
Your Applications & Infrastructure
              ↓
        Data Ingestion
              ↓
          Dynatrace
              ↓
      Analysis & AI
```

---

# Step 1: Select Your Technology

The first step is to tell Dynatrace what technology you want to monitor.

Examples include:

* AWS
* Azure
* Google Cloud
* Kubernetes
* OpenTelemetry
* Linux Servers
* Databases
* Applications

Dynatrace provides a Hub containing pre-configured integrations and setup guides for these technologies.

```text
AWS
Kubernetes
Azure
Databases
Applications
      ↓
    Dynatrace Hub
```

The Hub acts as a marketplace of integrations that simplifies setup.

---

# Step 2: Configure Your Environment

After selecting a technology, Dynatrace provides setup instructions.

For example:

### If monitoring a server:

```text
Install OneAgent
```

### If monitoring Kubernetes:

```text
Deploy Dynatrace Operator
```

### If using OpenTelemetry:

```text
Configure OTEL Collector
```

At this stage, you are connecting your infrastructure to Dynatrace.

```text
Infrastructure
       ↓
Configuration
       ↓
Dynatrace Connection
```

---

# Step 3: Start Sending Data

Once configuration is complete, data begins flowing into Dynatrace.

Data can be sent using:

### OneAgent

Automatically collects:

* Metrics
* Logs
* Traces
* Events

### OpenTelemetry

Collects observability data using open standards.

### APIs

Applications can directly send data through Dynatrace APIs.

### Manual Uploads

Certain data can also be uploaded manually.

```text
Applications
Servers
Containers
Databases
       ↓
OneAgent / OpenTelemetry / API
       ↓
Dynatrace Platform
```

At this point Dynatrace begins receiving telemetry data.

---

# Step 4: Verify Data Is Arriving

After connecting the environment, it is important to verify that Dynatrace is actually receiving data.

Dynatrace provides several tools for validation.

### Services App

Used to verify:

* Applications discovered
* Services detected
* Service health

```text
Frontend Service
Payment Service
Database Service
```

---

### Data Explorer

Used to verify:

* Metrics
* Logs
* Performance data

Example:

```text
CPU Usage
Memory Usage
Response Time
```

---

### Smartscape

Used to verify:

* Topology discovery
* Service dependencies
* Infrastructure relationships

Example:

```text
User
 ↓
Frontend
 ↓
API
 ↓
Database
```

---

### Discovery & Coverage

Used to check:

* Which systems are monitored
* Which systems are missing agents
* Overall monitoring coverage

```text
Covered Hosts: 95%
Uncovered Hosts: 5%
```

If data appears in these applications, the ingestion process is working correctly.

---

# Step 5: Visualize and Use the Data

Once data is successfully ingested, Dynatrace can start generating insights.

Users can:

### Create Dashboards

Monitor KPIs and system health.

Example:

```text
CPU Usage
Memory Usage
Error Rate
Revenue
```

---

### Configure Alerts

Receive notifications when issues occur.

Example:

```text
CPU > 90%
Response Time > 2 Seconds
```

---

### Use Davis AI

Davis AI can now:

* Learn baselines
* Detect anomalies
* Correlate events
* Identify root causes

Example:

```text
Database Latency
       ↓
Payment Failures
       ↓
Checkout Errors
```

Root Cause:

```text
Database Slowdown
```

---

# Complete Data Ingestion Workflow

```text
Step 1:
Select Technology
(AWS, Kubernetes, Azure, etc.)

          ↓

Step 2:
Configure Environment
(Install OneAgent / Configure OTEL)

          ↓

Step 3:
Send Telemetry Data
(Logs, Metrics, Traces, Events)

          ↓

Step 4:
Verify Data Arrival
(Data Explorer, Services, Smartscape)

          ↓

Step 5:
Analyze and Visualize
(Dashboards, Alerts, Davis AI)

          ↓

Anomaly Detection
Root Cause Analysis
Business Insights
```

# Summary

Data ingestion is the process of connecting applications, infrastructure, cloud services, and monitoring tools to Dynatrace. Organizations first select their technology, configure the connection, and begin sending telemetry data through OneAgent, OpenTelemetry, APIs, or other integrations. Once the data is received and verified, Dynatrace can visualize system behavior, build topology maps, detect anomalies, identify root causes, and provide actionable insights through Davis AI.
