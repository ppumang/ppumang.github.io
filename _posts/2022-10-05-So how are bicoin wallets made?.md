> For simplicity, only Type 2 Hierarchical Deterministic Wallets are considered


- In Bitcoin, **wallet** is a software that manages **keys**
- A user needs private key and public key to use bitcoin


<img src="../assets/images/t2_deterministic.png" title="px(픽셀) 크기 설정" alt="deterministic wallets"/><br/>

- A seed generates a master private key, and each private key can generate multiple child private key
- Each private key is used to make a seperate account
- Seeds are represented as word phrases like this


        army van defense carry jealous true
        garbage claim echo media make crunch


<img src="../assets/images/pvkey_pubkey_addr.png" title="px(픽셀) 크기 설정" alt="private key to address"/><br/>

- First, a private key is randomly generated
- A **private key** is transformed into **public key** and into **bitcoin address** respectively, by applying one way has function