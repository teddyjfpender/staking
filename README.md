To replicate the error, run:
- `scarb build && snforge test`

The error is:
```bash

error: Identifier not found.
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:5:5
use snforge_std::byte_array::try_deserialize_bytearray_error;
    ^*********^

error: Identifier not found.
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:6:5
use snforge_std::cheatcodes::events::Event;
    ^*********^

error: Identifier not found.
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:7:5
use snforge_std::{
    ^*********^

error: Identifier not found.
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:95:41
        Result::Ok(error) => assert_eq!(error, expected_error),
                                        ^***^

error: Type annotations needed. Failed to infer ?0.
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:111:35
    let mut data = raw_event.data.span();
                                  ^**^

error: Identifier not found.
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:156:30
        let token_contract = snforge_std::declare("DualCaseERC20Mock").unwrap().contract_class();
                             ^*********^

error: Ambiguous method call. More than one applicable trait function with a suitable self type was found: core::option::OptionTrait::unwrap and core::result::ResultTrait::unwrap. Consider adding type annotations or explicitly refer to the impl function.
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:156:72
        let token_contract = snforge_std::declare("DualCaseERC20Mock").unwrap().contract_class();
                                                                       ^****^

error[E0002]: Method `contract_class` not found on type `<missing>`. Did you import the correct trait and impl?
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:156:81
        let token_contract = snforge_std::declare("DualCaseERC20Mock").unwrap().contract_class();
                                                                                ^************^

error: Wrong number of arguments. Expected 1, found: 2
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:157:43
        let (address, _) = token_contract.deploy(@calldata).unwrap();
                                          ^***************^

error: Ambiguous method call. More than one applicable trait function with a suitable self type was found: core::option::OptionTrait::unwrap and core::result::ResultTrait::unwrap. Consider adding type annotations or explicitly refer to the impl function.
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:157:61
        let (address, _) = token_contract.deploy(@calldata).unwrap();
                                                            ^****^

error: Unexpected type for tuple pattern. "<missing>" is not a tuple.
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:157:13
        let (address, _) = token_contract.deploy(@calldata).unwrap();
            ^**********^

error: Variable "address" not found.
 --> /home/ubuntu/.cache/scarb/registry/git/checkouts/starknet-staking-fim25nqfrpqvm/526cb54/workspace/packages/contracts/src/test_utils.cairo:158:22
        TokenState { address, owner: *self.owner }
                     ^*****^

error: could not compile `example` due to previous error
[ERROR] Failed to build test artifacts with Scarb: `scarb` exited with error
```