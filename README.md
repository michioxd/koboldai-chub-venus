# KoboldAI for Chub Venus on Google Colab

By [michioxd](https://github.com/michioxd)

## Usage

### Browser setup

Because the CORS very stupid so we need disable them in Chromium (Chrome and another Chromium-based is fine but still recommend Chromium)

[Download Chromium](https://chromium.woolyss.com)

Linux:
```shell
chromium-browser --disable-web-security --user-data-dir="[some directory here]"
```

Windows:
- Right click to Chromium shortcut > Properties
- At Target, add this:

```powershell
 --disable-web-security --user-data-dir="[some directory here]"
```

It should be look like this:

```powershell
C:\Users\Administrator\AppData\Local\Chromium\Application\chrome.exe --disable-web-security --user-data-dir="[some directory here]"
```

Remember to change [some directory here] to another directory.

Like:

```
C:\Users\<yourusername>\ChromiumData
or
/home/<yourusername>/ChromiumData
```

### Cloudflare Tunnels Setup

- Go to [Zero Trust](https://one.dash.cloudflare.com)
- In sidebar, click Access > Tunnels
- Click Create a tunnel
- Name your tunel, then click Next
- Copy token (random string) from installation guide:
```shell
sudo cloudflared service install <TOKEN>
```
- Paste to cfToken
- Click next 
- Public hostname:

  Choose a domain (and subdomain if you want)

  **Remember:** Path must be empty

- Service section:

  **Type**: HTTP

  **URL**: `127.0.0.1:5000`

- Click Save tunnel

### Google Colab

Click in the given order

### Chub Venus setup

Remember to run Chub Venus in already disabled CORS browser

- Go to API Settings (click hambuger dropdown button)
- At API, select KoboldAI
- KoboldAI API URL set to your public hostname
- Click Check KoboldAI then click Save Settings

## KoboldAI still run in Read Only mode

- Go to your public hostname
- Click to AI button
- Select to another Modal, you can try (NFSW Models > Erebus 2.7B (NSFW))

**PLEASE NOTE:** Google only give 15GB VRAM

## Good luck :)
