# Tip4Serv Donation plugin for ARK SE

Create your ARK Survival Evolved shop with [Tip4serv.com](https://tip4serv.com/?ads=github) and monetize your community effectively. This addon connects your ARK Survival Evolved server to your online store, executing commands (group, money, items, etc.) in the server console following each donation.

![Tip4Serv](https://tip4serv.com/img/logo.png)

## Table of Contents

1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Installation](#installation)
4. [Commands](#commands-example)
    - [Broadcast](#broadcast)
    - [Sell Items and Experience](#sell-items-and-experience)
    - [Sell Points](#sell-points)
    - [Sell Subscriptions](#sell-permissions-for-subscriptions)
    - [Multiply Quantity](#multiply-quantity)
5. [Comparison: Plugin vs RCON](#comparison-plugin-vs-rcon)
6. [Support](#support)

## Introduction

This README provides detailed instructions on how to configure and utilize various commands and plugins for managing donations, item sales, experience points, and subscriptions on your ARK Survival Evolved server.

### HMAC Authentication

Tip4serv ensures secure communication by employing HMAC authentication, a robust method used by financial institutions. For more information, refer to the [HMAC Wikipedia page](https://en.wikipedia.org/wiki/HMAC).

## Prerequisites

- An ARK Survival Evolved server with [ARK Server API](https://gameservershub.com/forums/resources/ark-server-api.12/) installed if using this Tip4Serv plugin.
- RCON access to the server if using the RCON Tip4Serv connection.
- Installation of [ArkShop](https://gameservershub.com/forums/resources/ark-survival-evolved-arkshop.22/) and [Permissions](https://gameservershub.com/forums/resources/ark-permissions.20/) plugins if needed.

## Installation

1. **Create an Account:** Sign up at [Tip4serv.com](https://tip4serv.com/?ads=github).
2. **Add Your Server:** Navigate to [MY SERVERS](https://tip4serv.com/dashboard/my-servers) and add an ARK server.
3. **Choose Connection Method:** Select either the plugin or RCON.
4. **Configure Plugins:** Follow the provided instructions to set up the plugins.

## Commands Example

### Broadcast

Send a public thank you message in the server.

**Example:**  
- `Broadcast Thank you {arkse_username} for your {total_paid} {currency} donation`

### Sell Items and Experience

Provide players with items or experience.

**Prerequisites:**  
- Ensure the plugin is installed on the server where the player will receive their items.
- Check the **"Allow server choice"** option and select **"Run only if player is online"** in the product editor.
- Using this plugin you can also use self commands like **GiveItem** (impossible with RCON)
  
![Options](https://tip4serv.com/img/tuto/arksteamid.png)

**Examples:**  
- `GiveItemToPlayer {ue4_id} "Blueprint'/Game/PrimalEarth/CoreBlueprints/Resources/PrimalItemResource_ElementShard.PrimalItemResource_ElementShard'" 2 65 0`
- `GiveExpToPlayer {ue4_id} 50 false false`

Command generator: [ARK COMMANDS](https://arkids.net/commands)

### Sell Points

Add points to a player's account, allowing them to purchase in-game items.

**Prerequisites:**  
- [ArkShop plugin](https://gameservershub.com/forums/resources/ark-survival-evolved-arkshop.22/) is required.

**Example:**  
- `AddPoints {steam_id} 51`

### Sell Permissions for Subscriptions

Add or remove permissions for a player.

**Prerequisites:**  
- [Permissions plugin](https://gameservershub.com/forums/resources/ark-permissions.20/) is necessary.
- For multiple maps, add only one server in your product if all servers connect to the same database.

**Examples:**  
- `Permissions.Add {steam_id} VIP`
- `Permissions.Remove {steam_id} VIP`

**Procedure:**

1. Go to the [product editor](https://docs.tip4serv.com/store-setup/server-commands).
2. Enable subscriptions.
3. Configure the command to execute after payment.
4. Set up the command to execute when the subscription ends.

![Sub](https://tip4serv.com/img/tuto/arksubscription.png)

### Multiply Quantity

Multiply the quantity chosen by the customer using the following syntax: `{quantity*50}`

**Prerequisites:**  
- You must first enable the **"Allow quantity choice"** option in your product settings. 

**Use this command on Tip4serv if you wish to sell bundles of 200 points:**
- `AddPoints {steam_id} {quantity*200}`

**This command will execute in your server console after a purchase if a player buys the product four times:**
- `AddPoints 76561198030572988 800`

## Comparison: Plugin vs RCON

- **Plugin:**
  - Requires at least one player to be online for command execution.
  - Commands are executed by the buyer when you select the **"Run only if player is online"** option.

- **RCON:**
  - Ideal for adding points or managing subscriptions.
  - Commands are executed directly by the server and can run even if the server is empty.
  - Only commands compatible with `{steam_id}` or `{ue4_id}` can be used.

## Support

For any questions or assistance, please refer to the [Documentation](https://docs.tip4serv.com) or [Contact Us](https://tip4serv.com/contact).
