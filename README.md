# F2DateMinus

This module adds the ability to subtract dates from one
another to Flora-2.

This feature is not included in Flora-2, but is included in the commercially-available ErgoAI.

The code is probably not efficient.

It adds the following predicates:

`\date[|minus(\date)=>\duration|]`

`\date[|minus(\dateTime)=>\duration|]`

`\dateTime[|minus(\date)=>\duration|]`

`\dateTime[|minus(\dateTime)=>\duration|]`

`\date[|toDateTime=>\dateTime|]`

## Notes

`toDateTime` adds `0:0:0` (midnight) as the time. All versions of `minus` convert dates into dateTimes in this way, and then return the resulting duration.
