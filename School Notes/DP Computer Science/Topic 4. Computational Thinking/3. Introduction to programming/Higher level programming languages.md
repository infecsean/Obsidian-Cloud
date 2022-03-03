# Higher-level programming language
---
### Why do we need them?
- Since computers can only interpret 1s and 0s (machine language), its kinda hard for people to interpret.
- Eventually, binary code was replaced by mnemonics (instructions and reference to adress locations), later known as ==assembly language==, but these were still low level languages
- An assembler was required to convert assembly to machine language, but due to the ==lack of abstraction==, each assembly language was limited to a specific system
- This led to the need of developing on ==problem solving and efficiency==, higher-level languages

### What are high-level programming languages?
A programming language that:
- Uses elements of natural language
- easy to use
- facilitates [[Thinking Abstractly|abstraction]] by hiding parts of the system
- makes the programs simpler, faster, and more understandable

### How do we translate HLPLs to machine language? P243
- Since most stuff today are written in one of the HLPLs, ==translation== is required
- The translation process will convert the program into the machine language of the specific computer
- The program developed in an HLPL is called the ==source program/source code==
- The translated program in machine language is called ==object/target program==
- Translation uses two methods: ==Compilation== and ==interpretation==
- Compiler:
	- Translator that execute translation process ==once==
	- Translates ==source program== -> ==object program==
	- Object program is saved and no recompilation needed for future use
	- All errors are communicated to the programmer after the entire program is checked
	- Compilation ends when all syntax errors have been corrected
	- ==Faster than interpreters==
- Interpreter:
	- Translator that executes translation process ==everytime program is run==
	- Read each line of source program, analyze it, translate it into object program and execute it
	- Errors are communicated to the programmer for ==every instruction interpreted== 
	- 