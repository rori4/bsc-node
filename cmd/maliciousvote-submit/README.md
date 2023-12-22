## maliciousvote-submit
A tool for submitting the evidence of malicious voting

### Options
```
GLOBAL OPTIONS:
   --sender value    raw private key in hex format without 0x prefix; check permission on your own
   --node value      rpc endpoint, http,https,ws,wss,ipc are supported
   --chainId value   chainId, can get by eth_chainId (default: 0)
   --evidence value  params for submitFinalityViolationEvidence in json format; string
   --help, -h        show help
   --version, -v     print the version
```
### Evidence
can be extracted from logs generated by MaliciousVoteMonitor

### Example
```
./build/bin/maliciousvote-submit --chainId 714 --sender 59ba8068eb256d520179e903f43dacf6d8d57d72bd306e1bd603fdb812345678 --node ws://localhost:8545 --evidence "{\"VoteA\":{\"SrcNum\":6948,\"SrcHash\":\"dc58ff5dca8deefb7b03904ef2837e5f8b0e84ec147f021d4ff08343635540d3\",\"TarNum\":6949,\"TarHash\":\"24726f05534dc55c36ecc364951025abada0defa6d1b53bcb6b637f583b59996\",\"Sig\":\"9379a0626f962b828ed21fb34a6b6de034a23651c2e0c12b907293cf8f21d4fdd559e6f9c7f450a4243d33ad7aa5783d0e51e70979631d82819c254dfb130dfe924f057f7e2b4e64195fc7562f1cb0c45486c9cc3e6cc5679b4c0b5744bf33b5\"},\"VoteB\":{\"SrcNum\":6947,\"SrcHash\":\"24726f05534dc55c36ecc364951025abada0defa6d1b53bcb6b637f583b59996\",\"TarNum\":6950,\"TarHash\":\"6257f70ea6439b84d910595064a6e44e55ba0f2abc0c887346c420a60a5ef119\",\"Sig\":\"af9b500877d64277e80eea7c42b8d6ae5744d715625344ef6ddc66fa4e1dcb3e94568c79e018239641b724bacaa93046052d13f87b655d58b7afecf4e31036d5eca911e8c7436deea68c1e64ef7ed527ed25416039e4e7352f9b089cfb86481f\"},\"VoteAddr\":\"98b94137e4e2d4e628dcbc4a05d554f44950a7498040d3276d49c265708229127cd20e48c773cdc7a898b3bb572a17bf\"}"
```
