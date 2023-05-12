# Hello World

zk circuit implementation

## Description

zk circuit implementation using circom language and deploying on goerli chain to verify the proof 

## Getting Started
The project uses circom which requires rust environment which can be run on a wsl. 

### Executing program
circom code is first written implementing the logic gate with the help of templates from the 'circomlib' library. 

then the code is compiled generating r1cs file and wasm file. 

we compute the witness from the wasm file. 

Snarkjs is used to generate and validate proofs of witnesses. 
powers of tau ceremenoy is done. 
zkey is generated. 
proof is generated using zkey and witness output will be public input and output of the circuit
Verifying the proof requires a verification key, generated from the zkey, the proof, and the public inputs/output.

a verifier.sol file is generated which is deployed on the chain. 

after deploying, The inputs can be retrieved from the command: snarkjs generatecall

it should return true. 


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
