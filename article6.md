---
nav_order: 7
layout: default
title: Multi-Device Sync in the app
---
# Real-Time Financial Harmony: Understanding the Parallel Sync Engine
In a world where we switch between phones, tablets, and computers, your financial data cannot afford to be "stuck" on one device. The Falak Prakash Expense Tracker features a cutting-edge Parallel Sync Engine, designed to ensure your financial intelligence is available whenever and wherever you need it.

This isn't just a simple backup; it is a live, high-speed bridge between your local device and the cloud. Here is how we ensure your data is always accurate, secure, and synchronized.

## 1. The Hybrid Architecture
Unlike standard apps that rely on a single database, our app uses a Hybrid Cloud Architecture. We utilize both Firebase Realtime Database for instantaneous updates and Cloud Firestore for structured, long-term scalability. This dual-path approach ensures that even if one service experiences a delay, your data remains accessible and safe.

## 2. Parallel Synchronization (High-Speed Engine)
Time is money. Our latest update introduced the Parallel Sync Engine. Instead of syncing one item at a time (Expenses... then Stocks... then Loans...), our engine initiates multiple "lanes" of data transfer simultaneously.  

* **Zero-Lag Performance:** By using Kotlin Coroutines, the app reconciles all categories (from subscriptions to stock portfolios) at once.  
* **Efficiency:** This reduces the "sync window" by up to 70%, making the app feel snappy even when dealing with thousands of transactions.

## 3. Intelligent Conflict Resolution
What happens if you edit a transaction on your phone while your tablet is offline?  

* **The "Latest-Wins" Logic:** Our system automatically compares timestamps down to the millisecond. The most recent edit is preserved, ensuring you always see the latest truth.  
* **Manual Review:** For complex changes, the app identifies "Sync Conflicts" and flags them directly on your Main Screen, allowing you to manually choose which version to trust.

## 4. Privacy-First "Sync ID"
We value your privacy. The app utilizes a unique Sync ID system. 

## 5. Background Intelligence (WorkManager)
The sync feature doesn't stop when you close the app. Using Android’s WorkManager API, the tracker performs "Tombstone Reconciliation."  

* **Remote Deletions:** If you delete a record on one device, the background worker ensures that record is wiped from all your other devices automatically.  
* **Resilience:** If you lose internet connection, the app queues your changes and pushes them the moment you're back online.  
* **Anonymous Pairing:** You don't need to link a social media account to sync. Simply use your secure Sync ID on a second device, and the app instantly pairs your data.  
* **Encrypted Transport:** All data sent to the cloud is transmitted over secure SSL/TLS channels, ensuring your financial secrets remain yours.

## 6. The "Safety Net" Local Backup
While cloud sync is powerful, we believe in user autonomy. The Backup & Restore screen allows you to generate a Full JSON Export.  

* **Portability:** Download your entire financial history into a single, human-readable file.  
* **Merge Import:** When importing a backup, the app doesn't just overwrite your data; it intelligently merges it with your current records, keeping the most recent updates for every single entry.

<table border="0" cellpadding="10" cellspacing="0" width="100%" style="border-collapse: collapse;">
  <tr>
    <td valign="top" width="50%" style="padding: 10px;">
      <h2>How It works on Your Mobile Device</h2>
      <p>When you login, Falak Prakash's Firebase Realtime Database console marks you as a user. All of your data will sync between devices which are logged in with the same account.</p>
      <p><strong>See fig 6.1:</strong> This is firebase console. If you are a user, your UserId will be displayed in the list of users and your data will follow. For How to Login, see article 7 ("Our Login Feature")</p>
    </td>
    <td valign="middle" width="50%" style="padding: 0; background: #000;">
      <img src="assets/images/fig_6_1.png" alt="Figure 6.1" style="display: block; width: 100%; height: 100%; object-fit: cover;">
    </td>
  </tr>
</table>

## Why Our Sync Wins
The Parallel Sync Engine turns the Expense Tracker into a truly Multi-Device Powerhouse. It provides the peace of mind that your budget is always accurate, whether you're adding an expense at a grocery store or analyzing your stock portfolio from your couch.
