# Changelog

This project follows semantic versioning.

### unreleased
- [changed] Removed `feature(i128_type)` when running with the `i128` feature. Kept the feature flag
  for typenum to maintain compatibility with old Rust versions.
- [added] Integer `sqrt` to the `op!` macro.
- [added] Integer square root operator `SquareRoot` with alias `Sqrt`.

### 1.10.0 (2018-03-11)
- [added] The `PowerOfTwo` marker trait.
- [added] Associated constants for `Bit`, `Unsigned`, and `Integer`.

### 1.9.0 (2017-05-14)
- [added] The `Abs` type operater and corresponding `AbsVal` alias.
- [added] The feature `i128` that enables creating 128-bit integers from typenums.
- [added] The `assert_type!` and `assert_type_eq!` macros.
- [added] Operators to the `op!` macro, including those performed by `cmp!`.
- [fixed] Bug in `op!` macro involving functions and convoluted expressions.
- [deprecated] The `cmp!` macro.

### 1.8.0 (2017-04-12)
- [added] The `op!` macro for conveniently performing type-level operations.
- [added] The `cmp!` macro for conveniently performing type-level comparisons.
- [added] Some comparison type-operators that are used by the `cmp!` macro.

### 1.7.0 (2017-03-24)
- [added] Type operators `Min` and `Max` with accompanying aliases `Minimum` and `Maximum`

### 1.6.0 (2017-02-24)
- [fixed] Bug in `Array` division.
- [fixed] Bug where `Rem` would sometimes exit early with the wrong answer.
- [added] `PartialDiv` operator that performs division as a partial function -- it's defined only
  when there is no remainder.

### 1.5.2 (2017-02-04)
- [fixed] Bug between `Div` implementation and type system.

### 1.5.1 (2016-11-08)
- [fixed] Expanded implementation of `Pow` for primitives.

### 1.5.0 (2016-11-03)
- [added] Functions to the `Pow` and `Len` traits. This is *technically* a breaking change, but it
  would only break someone's code if they have a custom impl for `Pow`. I would be very surprised
  if that is anyone other than me.

### 1.4.0 (2016-10-29)
- [added] Type-level arrays of type-level integers. (PR #66)
- [added] The types in this crate are now instantiable. (Issue #67, PR #68)

### 1.3.1 (2016-03-31)
- [fixed] Bug with recent nightlies.

### 1.3.0 (2016-02-07)
- [changed] Removed dependency on libstd. (Issue #53, PR #55)
- [changed] Reorganized module structure. (PR #57)

### 1.2.0 (2016-01-03)
- [added] This change log!
- [added] Convenience type aliases for operators. (Issue #48, PR #50)
- [added] Types in this crate now derive all possible traits. (Issue #42, PR #51)
