# USDT Ethereum Transaction Script

This Python script allows you to send USDT (Tether) transactions on the Ethereum blockchain using the `web3.py` library. It connects to the Ethereum network via Infura and sends USDT from one wallet to another.

## Features
- Send USDT transactions on the Ethereum mainnet.
- Customizable gas price and gas limit.
- Secure transaction signing using a private key.

## Prerequisites
Before using this script, ensure you have the following:
1. **Python 3.x** installed on your machine.
2. An **Infura account** with a project ID (for Ethereum node access).
3. An **Ethereum wallet** with USDT balance and the private key.
4. Basic knowledge of Ethereum transactions and gas fees.

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/usdt-ethereum-transaction.git
   cd usdt-ethereum-transaction
   ```
2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration
1. Open the `send_usdt.py` file in a text editor.
2. Replace the following placeholders with your actual values:
   - `INFURA_URL`: Replace with your Infura project URL.
   - `PRIVATE_KEY`: Replace with your Ethereum wallet's private key (keep this secure!).
   - `SENDER_ADDRESS`: Replace with your sender wallet address.
   - `RECIPIENT_ADDRESS`: Replace with the recipient wallet address.
   - `USDT_CONTRACT_ADDRESS`: This is the USDT contract address on Ethereum (already provided).

   Example:
   ```python
   INFURA_URL = 'https://mainnet.infura.io/v3/YOUR_INFURA_PROJECT_ID'
   PRIVATE_KEY = 'your_private_key_here'
   SENDER_ADDRESS = '0xYourSenderAddress'
   RECIPIENT_ADDRESS = '0xRecipientAddress'
   ```

## Usage
1. Run the script:
   ```bash
   python send_usdt.py
   ```
2. The script will:
   - Send the specified amount of USDT.
   - Print the transaction hash.
   - Wait for the transaction to be confirmed on the Ethereum network.

## Customization
You can customize the following parameters in the `main()` function:
- `amount_to_send`: The amount of USDT to send.
- `gas_price_gwei`: The gas price in Gwei (adjust based on network congestion).
- `gas_limit`: The gas limit for the transaction (default is 60000).

Example:
```python
amount_to_send = 20  # Amount of USDT to send
gas_price_gwei = 10  # Gas price in Gwei
gas_limit = 60000    # Gas limit
```

## Important Notes
- **Security**: Never share your private key or commit it to version control. Use environment variables or a secure vault for production use.
- **Gas Fees**: Ensure your wallet has enough ETH to cover gas fees for the transaction.
- **Testnet**: For testing, you can use the Ropsten or Goerli testnet and update the `INFURA_URL` and `USDT_CONTRACT_ADDRESS` accordingly.

## Disclaimer
This script is for educational purposes only. Use it at your own risk. The author is not responsible for any loss of funds or unintended consequences.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Support
If you find this project helpful, consider giving it a ⭐ on GitHub. For questions or issues, please open an issue in the repository.



