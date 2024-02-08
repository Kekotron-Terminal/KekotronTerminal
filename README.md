# Kekotron Terminal

## Initial setup

  To download simply use `git clone`, or download as zip directly from the webpage.

  ![Untitled](https://github.com/Kekotron-Terminal/KekotronTerminal/assets/143968378/9aac3647-0b30-4847-a395-8b99562542df)


User Manual: https://docs.kekotron.io/setup

### 1. Open Kekotron
  Navigate to the appropriate OS directory, **right click `kekotron` and open.**

  Note: MacOS users may need to change their display settings for Kekotron to fit into the screen. Go to Settings > Display > click 'More Space'

  ![Untitled](https://github.com/Kekotron-Terminal/KekotronTerminal/assets/143968378/8aa87e9e-70a2-4ebd-8352-f1698485fd8f)

  Note: Linux users may need to run terminal command `./Kekotron` from the Kekotron_Linux directory if opening from GUI doesn't work 
  
### 2. Load wallets (optional in V2)

   **3 options**:
   * (Recommended) Use the wallet generator tool
     
     In the utilities panel, select the Create wallets tab, press Generate, then Save and Load, wallet keys will be saved in your Kekotron directory.
     
   * Make your own keyfile, put it somewhere in the Kekotron directory and point Kekotron to it in the `keyfile path` entry.

     The format must be one private key per line. Example:
     ```
     privatekey1
     privatekey2
     privatekey3
     ```
   * Enter a single private key into the `priv key input` entry.

### 3. Network (optional in V2)
A few public nodes are available to you by default when you first start Kekotron. They were selected for their robust privacy policy. You can try other nodes from this page if you desire. Note that **these nodes will only work in Call-saver mode.**
   
   In order to unlock the full power of Kekotron, you need to have a high quality PRC node to connect to. Public nodes such as infura and others listed above will **NOT** cut it.
   
   **Options**:
   * Local private node
      Running a Geth+lighthouse node using [NiceNode](https://www.nicenode.xyz/) on your machine(or local network) is the best way to get the outmost performace out of Kekotron. A simple sync in `snap` mode will be sufficient.

   * Remote private node
      A private node running remotely on a VPS and connected through SSH can also give you extremely high performance. Low cost options include [Contabo](https://contabo.com/) and [Hetzner](https://www.hetzner.com/)
     You can also chose to run Kekotron remotely directly into your VPS session if GUI is enabled.

   * Node provider
      You can also use a node provider. Right now the only free option that is recommended is [Alchemy](https://www.alchemy.com/pricing) free tier due to their robust burst limits. Chainstack, Quicknode, BlastAPI free tiers will NOT cut it(if Call-saver off).
     
Once you have a node ready, enter both the http and ws endpoints into the network section and turn off Call-saver mode in the settings.

Kekotron is set to run in Call-saver mode when you first run the application, this disables all features that depend on websocket connections, this includes most data feeds. To turn it off click the settings menu and uncheck the Call-saver box.

Poll rate can be reduced to your liking. Minimum value: 0.05s

### 4. Block explorer API keys
  It is recommended that you obtain a free API key from Etherscan, Arbiscan, etc. in order to allow Kekotron to fetch contract ABIs without rate limit.
  1. [Sign up on Etherscan](https://etherscan.io/register)
  2. Copy [your API key](https://etherscan.io/myapikey)
  3. Paste it into Kekotron settings menu, save.
<!-- -->
  1. [Sign up on Arbiscan](https://arbiscan.io/register)
  2. Copy [your API key](https://arbiscan.io/myapikey)
  3. Paste it into Kekotron settings menu, save.

## Usage
Simply enter contract addresses in the top bar to start interrating with it. This can be any type of contract. ERC20, ERC721, etc.

## optional - Virtualization
Some users may prefer to run Kekotron inside a virtual environnemnt.
**WARNING**: In some cases this can greatly degrade performance.
* Windows
  
  Use [Windows Sandbox](https://www.makeuseof.com/enable-set-up-windows-sandbox-windows-11/) for a simple, high performance virtual machine in just a few clicks. **Warning** data is destroyed every time you close Windows Sandbox. Make sure to save your keys if you chose to use it. 
* MacOS
  
  Use UTM to quickly spin up a high performance MacOS virtual machine. https://github.com/utmapp/UTM

---

