# Truth_Table_Generator
Converts a logical expression into its truth table.

DESCRIPTION:
This program generates a complete truth table for a given Boolean logic 
expression. It outputs a matrix with labeled headers, automatically 
detecting the number of variables (A, B, C, D) and handling intermediate 
negation columns.

FEATURES:
- Supports 2, 3, or 4 variables (A, B, C, D).
- Dynamic Headers: Columns are clearly labeled (e.g., "A", "NOT A", "RESULT").
- Smart Detection: Automatically adds columns for negated variables (e.g., A') 
  if they appear in the expression.
- Robust Parsing: Handles complex nesting and operator precedence.

------------------------------------------------------------------------
INSTALLATION:
------------------------------------------------------------------------
1. Open the HP Prime Connectivity Kit or the Program Editor on the calculator.
2. Create a new program named "Truth_Table_Generator".
3. Paste the source code into the editor.
4. Run the program from the User menu or by typing Truth_Table_Generator().

------------------------------------------------------------------------
INPUT SYNTAX:
------------------------------------------------------------------------
When prompted, enter your logic string using the following shorthand:

VARIABLES:
  A, B, C, D  (Case insensitive)

OPERATORS:
  AND      : n  (Think "Intersection")
  OR       : u  (Think "Union")
  NOT      : '  (Apostrophe/Single Quote, used as Postfix)
  XOR      : x
  IMPLIES  : >
  IFF      : =  (Equivalence)
  
GROUPING:
  ( )      : Standard parentheses

------------------------------------------------------------------------
EXAMPLES:
------------------------------------------------------------------------

1. Simple AND:
   Input: AnB
   Logic: A AND B

2. Implication with Negation:
   Input: A'>B
   Logic: (NOT A) IMPLIES B

3. Complex 3-Variable Logic:
   Input: (AxB)uC'
   Logic: (A XOR B) OR (NOT C)

4. Equivalence (IFF):
   Input: (AnB)=(AuB)
   Logic: (A AND B) IFF (A OR B)

------------------------------------------------------------------------
NOTES:
------------------------------------------------------------------------
- The program uses mathematical equivalents for logic. 
  "Implies" is calculated as logical comparison (A <= B).
  "IFF" is calculated as equality (A == B).
- "NOT" is strictly postfix. Write "A'", not "'A".
