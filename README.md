# Validate Bitcoin address
This is a collection of scripts to validate a bitcoin wallet address.

## Methodology

Check a Bitcoin address for its validity. This tool will see if the given string of text is indeed a correct and valid Bitcoin address. This tool can come in handy when verifying an address before sending any Bitcoins to it.

A bitcoin address uses a base58 encoding, which uses an alphabet of the characters 0 .. 9, A ..Z, a .. z, but without the four characters 0, O, I and l.

With this encoding, a bitcoin address encodes 25 bytes:

* the first byte is the version number, which will be zero for this task ;
* the next twenty bytes are a RIPEMD-160 digest, but you don't have to know that for this task: you can consider them a pure arbitrary data ;
* the last four bytes are a checksum check. They are the first four bytes of a double SHA-256 digest of the previous 21 bytes.

To check the bitcoin address, you must read the first twenty-one bytes, compute the checksum, and check that it corresponds to the last four bytes.

**Some key facts about valid Bitcoin addresses:**

 * A Bitcoin address is between 25 and 34 characters long;
 * the address always starts with a 1;
 * an address can contain all alphanumeric characters, with the exceptions of 0, O, I, and l.

## No-brainer ways

 1. You can type the address in [duckduckgo.com](https://duckduckgo.com) and see the details if it is a valid bitcoin address.
 2. Go [here](https://thomas.vanhoutte.be/tools/validate-bitcoin-address.php) and enter your
    address.

Collected from [rosettacode.org](https://rosettacode.org/wiki/Bitcoin/address_validation#PHP)
