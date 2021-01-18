# Conway File Parser
Rust library for parsing Conway Game of Life files.
## Expected file types
- [RLE (Run Length Encoded)](https://www.conwaylife.com/wiki/Run_Length_Encoded)
- [Plaintext](https://www.conwaylife.com/wiki/Plaintext)
- [Life 1.06](https://www.conwaylife.com/wiki/Life_1.06)
## Return data structure
Library will return a simple struct that contains two values:
1. Enum with the game type
2. A hashmap keyed with (X, Y) targets

Rational for the hashmap is to save on memory.  Loading up the entire game grid is wasteful, 
the engine on the other end will need to be able to handle dealing with a hashmap.