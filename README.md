# C.E.R Pattern
The C.E.R Pattern is a basic Command, Execution and Result pattern aimed at web technologies and game development.

## How does it work?
The CER Pattern works by stacking up commands in an aggregate then processing them using a command execution service. That service would then push out a result object based on what command was processed. Similar to CQRS the data written can be different to the data output from the execution process.

![Visual Process Chart](https://raw.githubusercontent.com/lparkermg/CERPattern/master/img/pattern.png)

_This is the basic visual process of how the CER Pattern works._

## What can it be used for?

The pattern itself can be used in a variety of applications and a few games as well.

Examples:

**Turn based strategy games** - A pattern like this would lend itself very well to games that involve stacking up commands (whether it's for automation or something different) since the results can be visual notifications etc.

**Any web based service** - An api could benefit greatly from a streamlined data flow where the results can be standardised with web responses or custom responses as needed.
