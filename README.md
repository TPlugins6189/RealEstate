# RealEstate
Rewrite of the abandoned HousePlugins from the ground up. Allows the buying of in-game houses existing on the map.

Documentation available here:
https://iceplugins.xyz/RealEstate

## How to install 0Harmony.dll
1. Download it (:D)
2. Copy the file
3. Paste to ...\Unturned\Unturned_Data\Managed

## Permissions
**realestate.maxhouses.[number]**
Sets the maximum number of houses for the permission holder. Repace [number] with a number.

**realestate.abandonhouse**
Gives access to /abandonhouse.

**realestate.addhouse**
Gives access to /addhouse. Should be admin only.

**realestate.buyhouse**
Gives access to /buyhouse.

**realestate.checkhouse**
Gives access to /checkhouse.

**realestate.evicthouse**
Gives access to /evicthouse. Should be admin only.

**realestate.removehouse**
Gives access to /removehouse. Should be admin only.

**realestate.bypass**
Allows users to bypass RealEstate barricade placing restrictions.

## Commands
**/abandonhouse**
Lets a player abandon the house that they are standing in. Requires the player to actually own the house. Permission: realestate.abandonhouse

**/addhouse**
Lets a player add the house that they are standing in to the catalog so that other players can buy it. Should be admin only. Permission: realestate.addhouse

**/buyhouse**
Lets a player buy the house that they are standing in. The house must be in the catalog. Permission: realestate.buyhouse

**/checkhouse**
Lets the player check the price and owner of the house that they are standing in. The house must be in the catalog. Permission: realestate.checkhouse

**/evicthouse**
Evicts the owner of the house that the player is standing in. Should be admin only. Permission: realestate.evicthouse

**/removehouse**
Removes the house that the player is standing in from the catalog. Should be admin only. Permission: realestate.removehouse

## Config
```
<?xml version="1.0" encoding="utf-8"?>
<RealEstateConfiguration xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <!-- Currency symbol used in RealEstate chat messages -->
  <currencySymbol>$</currencySymbol>
  <!-- Default max homes for people who don't have realestate.maxhouses.[number] -->
  <defaultMaxHomes>1</defaultMaxHomes>
  <!-- How often the plugin should check for and collect house payments in seconds. You can change this to a smaller or larger value if you'd like. -->
  <paymentCheckIntervalInSeconds>10</paymentCheckIntervalInSeconds>
  <!-- How often a player will pay the upkeep for their house in minutes. The money paid is the price of the house. IF YOU WANT TO DISABLE THIS, SET IT TO 0. -->
  <feePaymentTimeInMinutes>1440</feePaymentTimeInMinutes>
  <!-- If structures inside a home should be destroyed on an eviction. -->
  <destroyStructuresOnEviction>false</destroyStructuresOnEviction>
  <!-- If a player should not be allowed to build outside of his own home AT ALL. -->
  <disableBuildingIfNotInHome>false</disableBuildingIfNotInHome>
  <!-- If players should be allowed to build on vehicles -->
  <enableBuildingOnVehicles>false</enableBuildingOnVehicles>

  <!-- Ignore everything below this, it's used for data storage. -->
  <homes />
  <displayNames />
</RealEstateConfiguration>
```
