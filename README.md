## **Deploy an Encrypted Contract on Seismic Devnet**  

### **1️⃣ Install Dependencies**  

```bash
sudo apt update
sudo apt upgrade -y
sudo apt install -y curl git build-essential
```

```bash
sudo apt install file -y
```

```bash
sudo apt install unzip -y
```

### **2️⃣ Install Rust**  

```bash
curl https://sh.rustup.rs -sSf | sh
source "$HOME/.cargo/env"
rustc --version
```

### **3️⃣ Install jq (JSON Processor)**  

```bash
sudo apt install -y jq
jq --version
```

### **4️⃣ Install Seismic Foundry**  

```bash
curl -L \
     -H "Accept: application/vnd.github.v3.raw" \
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
```

```bash
source ~/.bashrc
```

⏳ **Note:** Foundry installation may take **15 minutes** to complete.

```bash
sfoundryup
```

### **5️⃣ Clone the Devnet Repository & Deploy the Contract**  

```bash
git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
cd try-devnet/packages/contract/
```

```bash
bash script/deploy.sh
```

### **6️⃣ Fund Your Wallet Address**  

- After running the deployment script, a **wallet address** will be displayed.  
- **Send 0.15 ETH from the Seismic faucet** to this address.  
- Press **Enter** after sending the funds.  

🖼️ **Example Output:**  
 ![seismicdev](https://github.com/user-attachments/assets/f9a7744d-06dc-4ecd-ac56-720bdb2eca5a)

### **7️⃣ Interaction with the Bun Contract**  

```bash
curl -fsSL https://bun.sh/install | bash
```

```bash
source ~/.bashrc
```

```bash
bun --version
```

```bash
cd ../cli/
bun install
```

📌 **Repeat the same steps**:  
- Send **some faucet funds** to the displayed address.  
- Execute the transaction:  

```bash
bash script/transact.sh  
```

---

✅ **Now, you've successfully completed the Seismic Devnet contract deployment and interaction!**  

⭐ **Don't forget to Star the Repo!**  
