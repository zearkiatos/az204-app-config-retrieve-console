# Retrieve configuration settings from Azure App Configuration

## Step 1: Create resource group

```sh
$ az group create --name myResourceGroup --location eastus
```

## Step 2: Declare variables

```sh
resourceGroup=myResourceGroup
location=eastus
appConfigName=appconfigname$RANDOM

# Print variable
$ echo $appConfigName
```

## Step 3: Registry provider

```sh
$ az provider register --namespace Microsoft.AppConfiguration
```

## Step 4: Checking estatus registration

```sh
$ az provider show --namespace Microsoft.AppConfiguration --query "registrationState"
```