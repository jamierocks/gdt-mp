gdt-mp Protocol Specificiation
==============================

## Current Protocol Version = 1

## Client -> Server

| Packet ID | Description | Field | Field Type | Notes |
| --------- | ----------- | ----- | ---------- | ----- |
| 0x00      | Client Identification | <ul><li>Packet ID</li><li>Username</li></ul> | <ul><li>byte</li><li>string</li></ul> | The client expects to recieve a server identification packet. |
| 0x01      | Set Game State | <ul><li>Packet ID</li></ul> | <ul><li>byte</li></ul> | This packet sets the game status (paused / unpasued) |

## Server -> Client

| Packet ID | Description | Field | Field Type | Notes |
| --------- | ----------- | ----- | ---------- | ----- |
| 0x00      | Server Identification | <ul><li>Packet ID</li><li>Protocol Version</li><li>Server Name</li></ul> | <ul><li>byte</li><li>int</li><li>string</li></ul> | Sent after recieving a client identification packet. |
| 0x01      | Save Information | <ul><li>Packet ID</li><li>Current Date</li><li>Employees</li></ul> | <ul><li>byte</li><li>string</li><li>string</li></ul> | As soon as the client recieves this packet, they are ready to begin playing. Where 'Employees' is a json array. |
