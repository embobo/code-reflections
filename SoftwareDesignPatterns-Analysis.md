# Software Design Pattern Analysis

Analysis of various software design patterns

## Table of Contents:
1. [Abstract Factory](#abstract-factory)

## Abstract Factory

- May 10th 2017
- [Reference](https://sourcemaking.com/design_patterns/abstract_factory)

#### Goal

To encapsulate platform dependencies and `new` statements.

#### Use (w/ example)

1. Define your platform dependent products. 

2. Create an abstract Factory class containing one method per product. Each method returns its promised product.

3. Create a derived Factory class per platform, implementing the methods according to the platform.

> Example
>
> **1. Define products:**
>
> * Serial port
> * Logger
> * Database
>
> **2. Create Abstract Factory with method per product:**
>
> Abstract Factory
> {
>
> * `SerialPort makeSerialPort()`
> * `Logger makeLogger()`
> * `Database makeDatabase()`
>
> }
>
> **3. Create Factory per platform:**
>
> * AbstractFactory : FactoryWin32
> * AbstractFactory : FactoryDarwin

#### Structure

[![img not found](https://sourcemaking.com/files/v2/content/patterns/Abstract_Factory.svg)](https://sourcemaking.com/files/v2/content/patterns/Abstract_Factory.svg)

