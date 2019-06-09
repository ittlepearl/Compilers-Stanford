Week 1: Introduction & the Cool Programming Language
# Introduction
Compiler: program -> (Compiler) -> executable + data -> output
(Fortran I : the first compiler)
Interpreter: program + data -> (Interpreter) -> output

# Structure of compiler
1. Lexical analysis
—> divide program text into words (similarly in reading English), or to be more formal, “tokens”.
Tokens include keyword (if, else, etc), variable names, blanks, semi colons..
2. Parsing
—> To understand sentence meaning
identify roles of words (article, noun, verb..) —> group words (subject, object) —> a tree with root being the sentence
—> break the sentence into a parsing tree
3. Semantic analysis
Try to understand the meaning to catch inconsistency —> but really hard
In English sentence, ambiguity might exist due to lake of context
In programming language, strict rules are applied (variable binding, type checking)
4. Optimization
Modify programs to run faster or use less memory.
Not always correct (x=y*0 optimized to x=0 is only valid when x and y are intergers) (If they are both float, NaN * 0 = NaN)
5. CodeGen ( code generation)
Produce assembly code

Modern compiler involves a lot of optimization ( other phases can be done quickly and easily)

# Economy of Programming Language
1.  Why there are so many languages?
Different domains have different needs:
Fortran (formula translation) is heavily used in scientific computing
SQL is used in business application
C/C++ is used in system programming

Application domains have conflicting needs
Programmer training is the dominant cost for a programming language

# COOL
###
class Main {
 i : IO <- new IO;
 main() : Int { {i.out_string(“Hello World”); 1;} }
}
###
Statement block (expression block) : evaluates the expression in order, the return value of the block is the value of last expression
—> 1 would return in the body of the method

To be succinct:
1. return type of main could be IO or Object so as to evict the last 1; statement
2. We could have (new IO).out_string() without allocating i in the beginning
3. Main object can inherit from IO class —> main gets all attributes and methods of IO class —> no need to new IO class object
