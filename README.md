## Donation plugin for ARK (Tip4Serv)

Create your ARK store with [Tip4serv.com](https://tip4serv.com/?ads=github) and monetize your community.
This addon connects your ARK Survival Evolved server to your online store and delivers orders (group, money, items...) after each donation by typing commands in the server console.

## HMAC authentication

Tip4serv adds a layer of security using HMAC authentication to communicate. It is a strong authentication method that is used by banks [HMAC WIKI](https://en.wikipedia.org/wiki/HMAC)

## Price

We take a 5% commission and that’s it ! You have access to all features with no subscription required.

## Features

Unlimited game servers & commands

Create subscriptions plan

Commands status tracking

Stock management

Deliver roles & messages on Discord

Easily offer a product to a friend

Create coupon code

Create discount

Add managers for your store

Purchase email and invoice

Sales statistics

Private flow for subscribers

Custom sub-domain

Resend commands

Customize store colors

No ads

## Store available in 15 languages

English, Danish, Dutch, French, German, Hungarian, Italian, Norwegian, Polish, Portuguese, Romanian, Russian, Spanish, Swedish and Turkish.

## Several payment methods

Here are the payment methods you can offer your players: Card, Paypal, Google Pay, Ideal, Giropay, Bancontact, Sofort, Sepa, EPS, BACS, Multibanco, BECS, Przelexy24, BOLETO, OXXO, Afterpay.

## Installation

Open an account on [Tip4serv.com](https://tip4serv.com/?ads=github) and add an ARK server in [MY SERVERS](https://tip4serv.com/dashboard/my-servers)

## Commands example

Here are some commands example you can use in the products configuration: [MY PRODUCTS](https://tip4serv.com/dashboard/my-products).
But you can use all commands of the plugins that you have installed on your server.

***Give 50 EXP to a player:***

`GiveExpToPlayer {ue4_id} 50 false false`

***Give Tek Sword to a player:***

`GiveItemToPlayer {ue4_id} "Blueprint'/Game/PrimalEarth/CoreBlueprints/Weapons/PrimalItem_WeaponTekSword.PrimalItem_WeaponTekSword'" 1 1 false`

***Add permission to a player:***

Required: ARK Permission plugin

`Permissions.Add {steam_id} vip`

***Add points to a player:***

Required: ARK Shop plugin

`AddPoints {steam_id} 51`

***Send message to all players:***

`Broadcast Thank you {arkse_username} for your {total_paid} {currency} donation`

[Check all commands here](https://arkids.net/commands)

## Quantity multiplier

You can also multiply the quantity choosen by the customer like this: {quantity*50}

Note: You must first activate the Allow quantity choice option in your product.

Use this command on Tip4serv if you want to sell bundles of 200 points:

`AddPoints {steam_id} {quantity*200}`

This will run in your server console after a purchase if the player buys product 4 times:

`AddPoints 76561198030572988 800`

## Need help?

[Documentation](https://docs.tip4serv.com)

[Contact us](https://tip4serv.com/contact)
