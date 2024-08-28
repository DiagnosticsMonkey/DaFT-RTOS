# What is an RTOS?

Let's start at the top.

An RTOS is a specialised operating system designed to provide greater determinism for responding to data or events.

## What is an OS?

An operating system is software which manages hardware and software resources. Typically, the operating system's primary role is to allocate resources between applications.  
E.g. slices of core execution time or space in memory.

## What is 'real-time'?

Real-time is a term used to define a system whereby there is a constraint, for example, between an event occurring to a system responding.  
Effectively from `trigger` to `reaction` within a `deadline`.

General operating systems don't typically guarantee a response within a given time period.

!> Whilst general OSes don't typically handle real-time, there are things you can do to improve behaviour in certain scenarios, such as adding pre-emption.  
This is beyond the scope of this documentation, but you can see some simple overview on [Wiki](https://en.wikipedia.org/wiki/Preemption_(computing)).

### Different types of real-time

Now that the concept of real-time has been introduced. It's time to break that down as not all scenarios are the same...

The subcategorisation is derived from the `impact` of a missed deadline.

<!-- tabs:start -->

### **Hard**

Hard real-time is the most strict. Deadlines `must` be met to ensure the proper functioning of critical applications. If a deadline is missed, the system will fail.

?> For example, air traffic control systems

### **Firm**

Firm real-time is where deadlines can be missed occasionally. In doing so, the quality of data or task may be degraded as information delivered after a deadline is treated as invalid. Meeting timing constraints is important for most tasks, as it directly impacts system performance and reliability.

?> For example, assembly lines

### **Soft**

Soft real-time is the least strict. The system can continue to function even if a deadline is missed. The result of a task or data may be impacted, but that data isn't critical. Effectively prioritising responsiveness but with flexibility in meeting deadlines.

?> For example, outputting video content

<!-- tabs:end -->
