# F2DateMinus

This module adds the ability to subtract dates and times from one
another in Flora-2.

Note that this implementation is likely less efficient than, and
may not be functionally identical to the implementation in ErgoAI.

It adds the following predicates:

`\date[|minus(\date)=>\duration|]`

`\date[|minus(\dateTime)=>\duration|]`

`\dateTime[|minus(\date)=>\duration|]`

`\dateTime[|minus(\dateTime)=>\duration|]`

Note that in date subtraction days are prioritized over months. So
March 30-February 28 will be `\du"P30D"` not `\du"P1M2D"`.

`\date[|toDateTime(\integer,\integer,\decimal)=>\dateTime|]`

Accepts hours, minutes, and seconds. Keeps the time zone in the date.

`\time[|toDateTime(\integer,\integer,\integer)=>\dateTime|]`

Accepts year, month, and day. Keeps the time zone in the time.

`\time[|minus(\time)=>\duration|]`

