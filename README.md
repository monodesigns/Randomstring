# Randomstring
[![Travis](https://img.shields.io/travis/monodesigns/Randomstring.svg?style=flat-square)](https://travis-ci.org/monodesigns/Randomstring)
[![License](https://img.shields.io/packagist/l/monodesigns/randomstring.svg?style=flat-square)](https://packagist.org/packages/monodesigns/randomstring)
[![Version](https://img.shields.io/packagist/v/monodesigns/Randomstring.svg?style=flat-square)](https://packagist.org/packages/monodesigns/randomstring)

## Installation
    composer require monodesigns/randomstring
  
## Usage
Randomstring is quite simple.
    
    use monodesigns\Randomstring;
    
    // default usage
    Randomstring::generate() // 'qfaP4A'
    
    // custom length (default = 6)
    Randomstring::generate(['length' => 4]) // '9suF'
    
    // custom types (default = 'upper lower number')
    Randomstring::generate(['types' => 'upper lower']) // 'hWVHkW'
    
    // all types (default = 'upper lower number')
    Randomstring::generate(['types' => 'all']) // 'I`}dlN'
    
    // hex
    Randomstring::generate(['hex' => true]) // 'e36ad8'
    
    // custom characters
    Randomstring::generate(['custom' => '!@']) // '1pZW!Y'

# Options
    Randomstring::generate([
      'length' => 6,
      'types' => 'upper lower number',
      'hex' => false,
      'custom' => ''
    ]);
    
    // get / set characters for different types
    Randomstring::$upper
    Randomstring::$lower
    Randomstring::$number
    Randomstring::$symbol
    Randomstring::$hex
    
If `hex` is true, it overrides anything set in the `types` option
