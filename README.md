# **eBay SOAP API – Order Fetching Tool (C# / .NET)**

A lightweight console application built in **C# / .NET** to fetch **eBay Orders** using the **eBay Trading API (SOAP)** with **OAuth Refresh Token** authentication.

This tool is ideal for developers who want a **simple reference implementation** or need to **test the eBay API quickly**.

---

## 🚀 **Features**

- ✔️ **OAuth authentication using Refresh Token**
- ✔️ **Fetch Order IDs from the last 30–90 days**
- ✔️ **Retrieve full order details**
- ✔️ **Pagination support**
- ✔️ **Transaction-level output**
- ✔️ **Clean, readable, fully commented code**
- ✔️ **Ready for database integration**

---

## 📦 **Technologies Used**

- **C# (.NET Framework / .NET Core)**
- **eBay Trading API SDK (SOAP)**
- **HttpClient** (for OAuth)
- **Newtonsoft.Json** (for OAuth parsing)

---

## 📘 **How It Works**

### **1️⃣ OAuth Access Token via Refresh Token**
The app sends the stored **refresh_token** to the eBay OAuth endpoint and retrieves a **new access_token**.

### **2️⃣ Fetch Order IDs**
Uses `GetOrdersCall` with:
- `TimeFilter` (last 30 days)
- Pagination (`EntriesPerPage`)
- Summary detail level (`ReturnSummary`)

### **3️⃣ Fetch Full Orders**
Loads all order details including:
- Buyer info  
- Payment & shipment status  
- Transaction list  
- Fees & totals  

Everything prints to the console.

---

## 📂 **Code Structure**
Program.cs

├── GetRefreshCode() → OAuth token generation

├── GetAllOrderIds() → Fetch only OrderIDs with pagination

├── GetAllOrders() → Fetch complete order details

├── OauthViewModal → OAuth response model


---

## 🔧 **Setup Instructions**

1. **Clone the repository**
2. **Open the solution in Visual Studio**
3. **Install eBay SOAP SDK**
4. Update your credentials inside the code:
   - **App ID**
   - **Cert ID**
   - **Refresh Token**
5. Run the console app  
6. View order output in terminal

---

## 📄 **Example Console Output**

OrderID: 12-34567-89012

BuyerUserID: test_user

TransactionID: 1290876543

ShippedTimeSpecified: False

## 🧑‍💻 **Author**

Umair Zafar

.NET Developer | API Integrations | eCommerce Solutions
