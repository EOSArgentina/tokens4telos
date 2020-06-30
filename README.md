# tokens4telos
This is a small modification of eosio.token smart contract.
The require_auth line at create action was deleted, and the RAM for creating a token
is paid by the issuer. These are the only changes. As a result, anyone can create a new token on this contract.


To create a new token use the command:

cleos -u https://api.eosargentina.io push action tokens4telos create '["your_account", "1000000000.0000 TOK"] -p your_account

This will create the token TOK with a maximum supply equal to 1000000000.0000 TOK.
The issuer will be "your_account".
