# concordium-env

Mainnet address for payment - 

## The following steps describe the procedure to setup the development environment for concordium:

### 1. Install Rust:
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
![Screenshot from 2023-02-14 23-29-59](https://user-images.githubusercontent.com/69577224/219132942-c4caf54f-2d9a-49c7-91b0-71f14600760f.png)

### 2. Install WASM to build contracts:
```bash
rustup target add wasm32-unknown-unknown
```
![Screenshot from 2023-02-14 15-42-37](https://user-images.githubusercontent.com/69577224/219133978-cf8037bb-c3f1-40a6-9150-33da9da8ccb3.png)

### 3. Install `cargo-concordium` for your system from [here](https://developer.concordium.software/en/mainnet/net/installation/downloads-testnet.html#cargo-concordium-testnet):
![image](https://user-images.githubusercontent.com/69577224/219135416-23292e25-4bcb-4bc6-849b-c6753e941a80.png)
Rename the downloaded file to `cargo-concordium`.
For Linux, go to the directory where the package is downloaded and run the following commands in the terminal to make it executable:
```bash
sudo chmod +x cargo-concordium
mv cargo-concordium ~/.cargo/bin
```
To ensure, everything was correct, run `cargo concordium --help` in the terminal and it should give an error free output.

### 4. Install Concordium Client:

Download the concordium client from [here](https://developer.concordium.software/en/mainnet/net/installation/downloads-testnet.html#concordium-node-and-client-download-testnet). Rename the package to concordium-client in case it has some version annotation.
![image](https://user-images.githubusercontent.com/69577224/219137819-9383c999-832d-40b2-aa5b-cd7b541c7832.png)

### 5. Make the package executable:

Go to the folder where you downloaded the concordium-client. If you are on Linux/Ubuntu/MacOS execute the following commands because the package is not yet executable.

![Screenshot from 2023-02-14 15-42-59](https://user-images.githubusercontent.com/69577224/219138302-61ec29c2-a047-488b-aec9-717b21164143.png)

### 6. Connect to the Testnet node:

```bash
concordium-client consensus status --grpc-port 10000 --grpc-ip node.testnet.concordium.com
```
Connect to the Testnet node:

![Screenshot from 2023-02-14 15-43-04](https://user-images.githubusercontent.com/69577224/219138723-81bb45ec-fa1b-4e88-b869-a6ecea925921.png)

### 7. Setup a wallet:

Get the official Concordium Wallet extension from [here](https://chrome.google.com/webstore/detail/concordium-wallet/mnnkpffndmickbiakofclnpoiajlegmg?hl=en-US).
Configure it to run on the Testnet as per the instructions [here](https://www.youtube.com/watch?v=wGLTV8MgLlA&list=PLU6SqdYcYsfJ27O0dvuMwafS3X8CecqUg&index=1).

### 8. Export the keys:

![image](https://user-images.githubusercontent.com/69577224/219141331-2937cb72-7142-4b09-86a5-239294b9be14.png)

### 9. Import your key into the concordium-client configuration:
![Screenshot from 2023-02-14 15-42-50](https://user-images.githubusercontent.com/69577224/219141529-87326af5-1c59-46d1-b788-fdc0d48329ae.png)
