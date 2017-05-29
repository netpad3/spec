netpad3
=======

UDP protocol, default port 6723

Each message contains at least 2 sections, separated by `;`.  Number of inputs should not change during a session, and will likely cause a reconnection.

### Section 1: Axes
List of axis values, from -32767 to 32767, separated by `,`

### Section 2: Buttons
Buttons specified as binary digits, with a leading 1, sent as hexadecimal.

*Example: `40`, meaning there are 6 buttons, but none are pressed*

Number of buttons can be derived via floor(log(value)/log(2))

### Additional sections
Remaining sections are identified by beginning with a type ID followed by a `:`.  None have been currently defined.
