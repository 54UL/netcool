## NETCODE SPEC DRAFT
RISC like netcode protocol spec.

## Instructions summary
- Data types and 'registers'
    - U8,U16,U64, IEE768-32, ANY
    - registers
        - Data maping
    - Handlers
        - Callbacks mapping
- Connection and auth
- RPC
    - Load and store
    - Control flow
- P2P
    - Load and store
    - Control flow
- Transactions
- Concurrency
- Crypto
- Database

## RPC(load and store) AND P2P INSTRUCTIONS CONCEPT(FICTIONAL CODE NOT EVEN THE FINAL FORM):

  1. **LD_SRPC**: Load from a remote server using RPC.

   ```
   LD_SRPC DESTINATION, SERVER_FUNCTION
   ```

   - `DESTINATION`: Register or memory location where the result will be stored.
   - `SERVER_FUNCTION`: The function or procedure to call on the remote server.

   2. **LD_CRPC**: Load from a remote server as a client using RPC.

   ```
   LD_CRPC DESTINATION, SERVER_FUNCTION
   ```

   - `DESTINATION`: Register or memory location where the result will be stored.
   - `SERVER_FUNCTION`: The function or procedure to call on the remote server.

3. **LD P2P Communication**:

   ```
   LD DESTINATION, PEER_IDENTIFIER, P2P_FUNCTION
   ```

   - `DESTINATION`: Register or memory location where the result will be stored.
   - `PEER_IDENTIFIER`: The identifier of the peer you want to communicate with.
   - `P2P_FUNCTION`: The specific peer-to-peer function or operation you want to perform.
