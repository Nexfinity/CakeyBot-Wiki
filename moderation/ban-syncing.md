---
title: Ban Syncing
description: 
published: 1
date: 2024-01-09T06:41:38.096Z
tags: 
editor: markdown
dateCreated: 2023-12-20T10:18:18.508Z
---

# Overview
The "Ban Sync" feature in Cakey Bot offers server owners an efficient and synchronized method to manage bans across multiple servers within a designated pool. This feature significantly streamlines moderation efforts and maintains consistency in enforcing bans across interconnected communities.

# How It Works
* **Server Pool Creation:** Server owners initiate the ban synchronization process by creating a designated pool of servers through the [web dashboard](https://cakey.bot/dashboard/public/).

* **Ban Replication:** When a user receives a ban within a server in the established pool, the bot identifies and replicates this ban, swiftly implementing the same action across all other connected servers.

* **Quick Updates:** The Ban Sync feature processes bans via a queue which prevents the bot from being restricted by ratelimits. However, bans are also checked when a user joins the server allowing almost real-time enforcement by banning users instantly who have not been processed by the queue yet.

* **Multi-Way Syncing:** Within a designated pool, bans are synchronized across all servers, irrespective of the server where the ban was initially issued. This means bans will sync across all servers within the pool even if the ban did not originate in the server that created the pool.

# Creating a Pool
> Currently severs are limited to creating 1 pool per server. However, servers can be incldued in any number of pools.
{.is-info}

To create a new pool simply login to the web dashboard and follow these steps:
1. Open the "Ban Sync" page 
2. Click the "Create New Ban Sync Pool" button
3. Once the creation modal opens, enter a name and click the "Create" button

You have now created you first ban sync pool. Read the section below to add servers to your newly created pool.

# Toggling Ban Sync Feature
By default servers are NOT allowed to be added to pools. In order to allow the server to be added to a pool, you will need to click the "Enable Ban Sync for this server" button on the Ban Sync page. 

You will need to enable ban sync for every server you wish to add to a ban sync pool.

**Note:** Once the server has been added to a pool you can disable this toggle again to prevent the server from being added to other pools. This toggle will NOT remove servers from existing pools, it only prevents the server from being added to new pools.

# Adding Servers to Pools
> Currently only 3 servers can be added to a pool.
{.is-info}

While on the Ban Sync page follow these steps:
1. Click the grey box inside of the selected pool under the text "Servers:"
2. This should bring up a selection menu for all of the servers that you are in
3. Select the servers you wish to add to the pool, they will automatically be added

> By default, servers will NOT be able to be added to Ban Sync pools. You will have the manually toggle this to be "Enabled" on each server you wish to add.
{.is-warning}

# Removing Servers from Pools
> Only the server that created the pool can remove servers from the pool. Servers that have been added to the pool can choose to "leave" the pool however.
{.is-info}

While on the Ban Sync page follow these steps:
1. Inside the grey box under the text "Servers:" you will see a lsit of servers in the pool
2. Click the white "X" button for any servers you wish to be removed.
If you do not see the white "X", then you are likely viewing the pool from a server that was added to the pool and not from the server that created the pool.

# Leaving a Pool
> Servers that create a pool will only be able to delete the pool, they can not leave the pool.
{.is-info}

Servers that have been added to a pool will be able to see that they have been added to the pool. In addition to this, they will be able to leave the pool. Servers that are added to pools will not be able to edit other servers in the pool or delete them. Only the server that created the pool will be able to manage it. To leave a pool simply click the orange "Leave" button at the bottom of the pool.