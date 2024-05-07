# 🚀 Installation

First, make sure you are a member of our [official discord server](https://discord.raulex.com) and have a trial or full version of [Raulex KeyCard Rooms](https://discord.com/channels/879567396472500244/1231621287227556001) which you have bought from our user panel.

<div align="center">

<figure><img src="../../.gitbook/assets/ehx8gk0.png" alt="" width="188"><figcaption><p><a href="https://discord.raulex.com">Join our discord server</a></p></figcaption></figure>

</div>

## Pre-requisites

* Create an [application ](../../user/console/creating-an-application.md)in your [user panel](../../user/console/access-your-console.md) in our discord.
* Make sure you have added **Keycard Rooms** as **service** for your **application**.

## Installation

### Step 1. Install the mod <a href="#install-the-mod" id="install-the-mod"></a>

There are **two methods** to install the mod on to your server.

#### &#x20;Method 1: Through Steam Workshop

Install [Raulex KeyCard Rooms](https://steamcommunity.com/sharedfiles/filedetails/?id=3229535788) and [RaulexCore](https://steamcommunity.com/sharedfiles/filedetails/?id=3229896741) from Steam Workshop just like any other mod.

<figure><img src="../../.gitbook/assets/image (9).png" alt="" width="563"><figcaption><p>Steam workshop mod</p></figcaption></figure>

#### Method 2: Through [console](../../user/console/access-your-console.md).

You can download the PBOs from your console through your console and add it to your modpack.

* Make sure you have added both <mark style="color:orange;">**RaulexCore**</mark> and <mark style="color:orange;">**RaulexKeyCardRooms**</mark> to your modpack.

<figure><img src="../../.gitbook/assets/Untitled (3).png" alt=""><figcaption><p>Download <strong>PBOs</strong></p></figcaption></figure>

### Step 2. Set your application credentials.

Start your server for the first time after you have installed the mod, this will generate a profiles folder called **RaulexCore**.

1. Click on the <mark style="color:orange;">View API Key</mark> button to get **apikey** for your application.

<figure><img src="../../.gitbook/assets/Untitled (2).png" alt=""><figcaption><p><strong>View API Key</strong> button in your application panel.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption><p>API Key shown once <strong>View API Key</strong> is clicked.</p></figcaption></figure>

2. Now copy both your **appId** and **apiKey** to your **config.json** inside **RaulexCore** in your profiles folder.

<figure><img src="../../.gitbook/assets/Screenshot 2024-05-07 195355.jpg" alt=""><figcaption><p><mark style="color:orange;">RaulexCore</mark> generated in profiles folder</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-05-07 200231 (1).jpg" alt=""><figcaption><p>Open <mark style="color:orange;"><strong>config.json</strong></mark> inside <mark style="color:orange;"><strong>RaulexCore</strong></mark></p></figcaption></figure>

Change your config.json so that it looks like this (Fill in your own **appId** and **apiKey**):

```json
{
    "appId": "raulex-app-07efda3b-0033-43f9-a147-XXXXXXXXXX",
    "apiKey": "raulex-api-key-94983413-7f86-4285-9807-XXXXXXXXXX",
    "forceShutDownOnFailure": 1
}
```

### Step 3: Restart your server

Now you should be **able** to **boot** your server without getting **terminated**.
