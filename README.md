# 💼 ESX Billing System (Invoices)

A lightweight and user-friendly billing system for FiveM using ESX, supporting both immediate and due-based invoices. Easily integrated with [`ox_lib`] for modern UI and notification support.

## 🔧 Features

- Create and issue invoices to players (cash or bank payment)
- View and pay personal invoices
- Job-based access control for invoice creation
- Interest-based overdue system (optional)
- Admin command to check invoices of other players
- Clean UI via `ox_lib` context menus and dialogs
- Server and client-side logic included

## 📦 Requirements

- [ESX Legacy](https://github.com/esx-framework/esx-legacy)
- [ox_lib](https://overextended.github.io/ox_lib/)
- MySQL (via `mysql-async` or `oxmysql`)

## ⚙️ Configuration

Make sure to define the allowed job names in your `Config`:

```lua
Config = {
    BillingJobs = { "police", "ambulance", "mechanic" }, -- Jobs that can issue invoices
    CheckBillAllowedJobs = { "police", "ambulance" },    -- Jobs that can view player invoices
    InvoiceDays = 172800000, -- 2 days in milliseconds
    InvoiceIncrease = 100    -- $ amount added every period for due invoices
}

