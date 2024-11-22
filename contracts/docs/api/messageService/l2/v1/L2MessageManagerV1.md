# Solidity API

## L2MessageManagerV1

### INBOX_STATUS_UNKNOWN

```solidity
uint8 INBOX_STATUS_UNKNOWN
```

The 3 status constants for L1 to L2 message statuses.

### INBOX_STATUS_RECEIVED

```solidity
uint8 INBOX_STATUS_RECEIVED
```

### INBOX_STATUS_CLAIMED

```solidity
uint8 INBOX_STATUS_CLAIMED
```

### inboxL1L2MessageStatus

```solidity
mapping(bytes32 => uint256) inboxL1L2MessageStatus
```

_Mapping to store L1->L2 message hashes status.
messageHash => messageStatus (0: unknown, 1: received, 2: claimed)._

### _updateL1L2MessageStatusToClaimed

```solidity
function _updateL1L2MessageStatusToClaimed(bytes32 _messageHash) internal
```

Update the status of L1->L2 message when a user claims a message on L2.

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| _messageHash | bytes32 | Hash of the message. |
