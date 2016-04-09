gdt-mp Protocol Specificiation
==============================

## Client -> Server

| Packet ID | Description | Field | Field Type | Notes |
| --------- | ----------- | ----- | ---------- | ----- |
| 0         | Client Identification | <ul><li>Packet ID</li></ul> | <ul><li>byte</li></ul> | The client expects to recieve a server identification packet |

## Server -> Client

| Packet ID | Description | Field | Field Type | Notes |
| --------- | ----------- | ----- | ---------- | ----- |
| 0         | Server Identification | <ul><li>Packet ID</li></ul> | <ul><li>byte</li></ul> | Sent after recieving a client identification packet. |
