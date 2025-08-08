HC1T1 - Task 1: Function Composition

```haskell
-- Define a function that multiplies a number by 2
double :: Int -> Int
double x = x * 2

-- Define a function that increments a number by 1
increment :: Int -> Int
increment x = x + 1

-- Use function composition to apply 'double' first, then 'increment'
doubleThenIncrement :: Int -> Int
doubleThenIncrement = increment . double

-- Example usage in main
main :: IO ()
main = do
    let x = 5
    putStrLn ("Original: " ++ show x)
    putStrLn ("Double: " ++ show (double x))
    putStrLn ("Increment: " ++ show (increment x))
    putStrLn ("Double then Increment: " ++ show (doubleThenIncrement x))
```

### How it works:

* `double x = x * 2`: Multiplies the input by 2.
* `increment x = x + 1`: Adds 1 to the input.
* `doubleThenIncrement = increment . double`: Uses function composition. This means:

  * First apply `double` to the input.
  * Then apply `increment` to the result.

### Run the Code:

If you compile and run this in GHC or an online Haskell compiler, the output will be:

```
Original: 5
Double: 10
Increment: 6
Double then Increment: 11
```

