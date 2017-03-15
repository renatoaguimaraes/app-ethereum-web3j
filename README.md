# ethereum-web3j
Ethereum client.


### Transacion listener example.

The code below connects on http://localhost:8545/ to show all transaction attributes received.

```java
Web3j web3 = Web3j.build(new HttpService());

web3.transactionObservable().subscribe(tx -> {
    System.out.println("------------------");
    System.out.println("Block hash " + tx.getBlockHash());
    System.out.println("Block number " + tx.getBlockNumber());
    System.out.println("Creates " + tx.getCreates());
    System.out.println("From " + tx.getFrom());
    System.out.println("Gas " + tx.getGas());
    System.out.println("Gas price " + tx.getGasPrice());
    System.out.println("Hash " + tx.getHash());
    System.out.println("Input " + tx.getInput());
    System.out.println("Nonce " + tx.getNonce());
    System.out.println("Public key " + tx.getPublicKey());
    System.out.println("R " + tx.getR());
    System.out.println("Raw " + tx.getRaw());
    System.out.println("S " + tx.getS());
    System.out.println("To " + tx.getTo());
    System.out.println("Transaction index " + tx.getTransactionIndex());
    System.out.println("Value " + tx.getValueRaw());
});
```

