# Programming Game AI By Example

## Book Info

[Programming Game AI by Example - Mat Buckland @ 2005](https://www.jblearning.com/catalog/productdetails/9781556220784#productInfo)

where you can get the Source Code

## Need Install & Environment

For FIPS: python + cmake

For LuaBind Demo: add environment variable --

* BOOST_1_48_0_INCLUDE_PATH: path/to/boost_1_48_0
* BOOST_1_48_0_LINK_PATH: path/to/boost_1_48_0/stage/lib

If you want to build boost yourself, please install VS2010.

The version of LuaBind is old, so is the boost ...

## Build

```
cd code && fips build win_d
```

build config: code/fips-configs/win_d.yml (with VS2017 32bit)