# Buffer-overflow-challenge
## The challenge works only in Windows OS!!
A little fun challenge to test your hacking skills

# How to start the challenge:
  1. Download the repository.
  2. Run rop.exe from your command line.

## Now the challenge begins:
  Try to make the program print your ID (consider using the source code in the repository when needed).

### Hints:
  1. Try using the gadgets in a1 function.
  2. ASLR is off, so you can enter the exe file into IDA to find symbols.
  3. It's recommended to use the given exe file and not recompile. If you do decide to recompile, please don't turn off DEP, and do turn off ASLR and stack cookie. Also compile it in debug so the a1 function doesn't disappear.
  4. The general idea should be to inject a string constructed by:
     1. Overriding the buffer.
     2. Use a1 gadgets to write into writable memory.
     3. Use printf to print from the address we wrote to your ID.
     4. Exit the program.
