# C.E.R Pattern
The C.E.R Pattern is a basic Command, Execution and Result pattern aimed at web technologies and game development.

## How does it work?
The CER Pattern works by stacking up commands in an aggregate then processing them using a command execution service. That service would then push out a result object based on what command was processed. Similar to CQRS the data written can be different to the data output from the execution process.

![Visual Process Chart](https://raw.githubusercontent.com/lparkermg/CERPattern/master/img/pattern.png)

_This is the basic visual process of how the CER Pattern works._

## What are the different parts?

**Command Object:** The command object is where the input data is sent to the Execution process(es). The object itself can hold data but not run anything at all since running anything would have to happen within the execution part of the pattern, this includes the command validation.

**Execution Process(es):** The execution process(es) are where the commands get stored, then filtered to the specific execute handler and then validated and processed. The execution process basically handles what ever needs to be done by the command like store data, load data, move something etc, then once the process has finished it spits out the results object. The execution process could be made to be async and spawn x amount of threads if needed.

**Results Object:** The Result object is where the data (along with any error data) from the execution process is put before it's sent to be read by the client. It can be expanded on but is required to have a reason phrase and status code in it this is mainly for ease of use when working with web based systems. 

## What can it be used for?

The pattern itself can be used in a variety of applications and a few games as well.

Examples:

**Turn based strategy games** - A pattern like this would lend itself very well to games that involve stacking up commands (whether it's for automation or something different) since the results can be visual notifications etc.

**Any web based service** - An api could benefit greatly from a streamlined data flow where the results can be standardised with web responses or custom responses as needed.
