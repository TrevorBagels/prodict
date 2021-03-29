### This is a fork of [prodict](https://github.com/ramazanpolat/prodict). It now supports python 3.9, and it has a few other changes that I'll describe below.

## Changes

 * Lists of prodicts work again
 * Prodicts within prodicts works again (I can't remember if that was actually an issue, but it might have been so I'm noting it as a change)
 * Dictionaries of prodicts are now supported
 * Enums are also supported, even after being serialized and deserialized by JSON

Those are all the changes that come to mind, for more documentation, I highly recommend viewing the [original repository](https://github.com/ramazanpolat/prodict).

## Some examples

Example of a dictionary of prodicts
```
from prodict import Prodict
from enum import IntEnum

class SomeEnum(IntEnum):
	WHAT		= 0
	SOMETHING	= 1
	HELLOTHERE	= 2

class Thing(Prodict):
	some_number:	int
	some_string:	str
	some_enum:	SomeEnum

class AnotherThing(Prodict):
	some_dict:	dict[str, Thing] #this will create a dictionary of prodicts, more specifically, Things. 
```
