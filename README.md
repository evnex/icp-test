# 📦 Take-Home Test: Bulk ICP Dashboard

## 🏢 Background

**Evnex** is New Zealand’s leading electric vehicle charging manufacturer.

Every day, our operations team processes 1,000+ ICP (Installation Control Point) codes to:
- ✅ Verify meter connection details  
- 🔄 Manage switch-in progress for new customers  
- 🧰 Troubleshoot network issues  

Currently, this is done manually by uploading CSVs and copy-pasting each ICP into the [EMI ICP Connection Data API](https://emi.developer.azure-api.net/api-details#api=ICP-connection-data-v2&operation=56fd9f8fea9dce11ec5eee7f). We're building a dashboard to automate and streamline this workflow.

---

## 🧠 Your Task

Build a **Bulk ICP Dashboard** for internal use. This tool should:
- Upload a CSV of ICP codes
- Fetch ICP connection data in **bulk** via the `/ICPConnectionData/v2/list` API
- Display results in a **sortable and filterable** table
- Show **summary insights** above the table

> 🔧 If the API isn’t working for you, feel free to **mock the responses**.
>
> 🔑 You can [sign up for API access here](https://emi.developer.azure-api.net/signup).  
> 📄 You can also [check out the API documentation here](https://emi.developer.azure-api.net/api-details#api=ICP-connection-data-v2&operation=56fd9f8fea9dce11ec5eee7f).

---

## 💻 Front-End UI Requirements

### 📤 CSV Upload
- Drag-and-drop or file picker
- Parse the **first column** of the CSV as an array of ICP codes

### 📋 Results Table

Each row should include:
- **ICP**
- **Address** (`PropertyNameOrDescription` + street)
- **NetworkParticipantName**
- **MeterInstallationDate**
- **TraderSwitchInProgress**

**Table features:**
- ✅ Sort by any column
- 🔍 Filter by `TraderSwitchInProgress` status (true/false)

### 📊 Summary Cards (above the table)
- Total ICPs processed
- Number of ICPs with `TraderSwitchInProgress = true`
- Earliest `InitialElectricallyConnectedDate`

---

## 🧪 Notes & Expectations

- Treat this as if it's headed to production: clean, tested, maintainable code.
- Use any language, framework, or libraries you like.
  > We use **React**, **TypeScript**, and **Material UI** internally—but use what you’re most productive with.
- Timebox: **No strict limit**—see how far you get. The goal is to see your thinking, not perfect completion.

---

## 📤 Submission

- Submit your project via **GitHub**
- Include a `README.md` with:
  - Setup instructions
  - How to run the app
  - Any assumptions or notes you'd like to share

---

### 🚀 Questions?

We're happy to help—just reach out if you need clarification. Looking forward to seeing what you create!
