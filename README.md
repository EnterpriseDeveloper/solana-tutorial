# buildspace Solana GIF Portal Project

### **Welcome 👋**
To get started with this course, clone this repo and follow these commands:

1. Run `npm install` at the root of your directory
2. Run `npm run start` to start the project
3. Start coding!

### **What is the .vscode Folder?**
If you use VSCode to build your app, we included a list of suggested extensions that will help you build this project! Once you open this project in VSCode, you will see a popup asking if you want to download the recommended extensions :).



### **Questions?**
Have some questions make sure you head over to your [buildspace Dashboard](https://app.buildspace.so/courses/CObd6d35ce-3394-4bd8-977e-cbee82ae07a3) and link your Discord account so you can get access to helpful channels and your instructor!

### Generate new Solana contract
1. Generate new project `anchor init myepicproject --javascript`
2. Create new wallet that will store localy `solana-keygen new`
3. Check wallet that was generated `solana address`
4. Run tests `solana address`

### **Deploy on test net?**
1. Switch to the devnet `solana config set --url devnet`
2. Check if everything fine `solana config get`
3. Get 2 fake tokens from airdrop `solana airdrop 2`
4. Check balance `solana balance`
5. Build `anchor build`
6. In Anchor.toml, change [programs.localnet] to [programs.devnet]. Then, change cluster = "localnet" to cluster = "devnet".
7. Get ganereted addrss `solana address -k target/deploy/myepicproject-keypair.json`
8. Copy id and go to the `myepicproject/programs/myepicproject/src/lib.rs` and change id.
9. Now, go to Anchor.toml and under [programs.devnet] you'll see something like myepicproject = "Fg6PaFpoGXkYsidMpWTK6W2BeZ7FEfcYkg476zPFsLnS". Go ahead and change this id to the same id output when you run solana address -k target/deploy/myepicproject-keypair.json.
10. Run again `anchor build`
11. Deploy `anchor deploy`
12. Check status `https://explorer.solana.com/address/DT3rnDBUi1WmafAFsNLVnNbPfNRJZ54t2x8NppY58ALi?cluster=devnet`
13. Send token to address `solana airdrop 2 EWbEMg4RgQWnhJZ2gNb2BeY82oVuQnzXieQUwdPXPxts --url devnet`