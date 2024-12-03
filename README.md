## AIGAEA NETWORK BOT

**AIGEA BOT USING PROXY**

![banner](assets/image2.png)

This is a proxy manager script that interacts with Aigaea's API, allowing you to authenticate with proxies, track scores, and manage browser sessions. The script fetches proxy lists and pings them periodically while managing authentication sessions.

- [Register Here](https://app.aigaea.net/register?ref=gauvzAZi8GQyog)

## Prerequisite

- Node.js (v16 or above)
- npm (Node Package Manager)
- Aigaea account (for obtaining the access token)

## Installation

1. **Clone the repository or download the script**:
   ```bash
   git clone https://github.com/Rambeboy/aigaea-network-bot.git && cd aigaea-network-bot
   ```

2. **Install dependencies**:

   The script requires several packages such as `node-fetch`, `https-proxy-agent`, and `readline`. You can install these by running:

   ```bash
   npm install
   ```

3. **Configure your accounts**
   ```bash
   cp config/proxy_list_tmp.js proxy_list.js
   ```

   The necessary packages will be listed in `package.json`.

4. **Create the `proxy_list.js` file**:

   ```bash
   nano proxy_list.js
   ```

   The proxy list will be saved to this file, put your proxy there.


## Access Token and first 8 browserID

- You can obtain your token and browser id from the [Aigaea Dashboard](https://app.aigaea.net/register?ref=gauvzAZi8GQyog).

  ![gaea-token](assets/image-1.png)

- Copy your first 8 browser id

  ![image](https://github.com/user-attachments/assets/15f23b20-951a-4963-91f3-2277b9db1b26)


## Running the Script

1. **Run the script**:

   After installing the dependencies and setting up the `proxy_list.js` file, you can run the script using Node.js:

   ```bash
   npm run start
   ```


## How It Works

**Proxy Authentication and Pinging**:
- The script authenticates with Aigaea using your access token.
- It retrieves a `browser_id` for each proxy, which is stored for future use.
- Periodically, the script pings the proxies to ensure they are still functional and have a high score.
- If a proxy's score falls below a certain threshold, it will re-authenticate and retry the ping process.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
