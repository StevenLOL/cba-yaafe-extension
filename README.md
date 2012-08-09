CBA-YAAFE-extension
===================

This is an extension for [YAAFE](http://yaafe.sourceforge.net) (Yet Another Audio Feature Extractor), developed for music detection with the **Continuous Frequency Activation feature** (CFA) for the **Cultural Broadcasting Archive** ([CBA](http://cba.fro.at)).

## Adaptations

This extension provides the possibility to get the output directly to the commandline for implementing it e.g. in PHP:

> <code>
> $cmd = 'yaafe_cba.py -r 11025 --resample -f "cfa: ContinuousFrequencyActivation" wavefile.wav';
> </code>  

> <code>
> exec( $cmd, $output, $return_value);
> </code>

## New Features

For a list of the new features and a description see: *[FEATURES.md](https://github.com/mcrg-fhstp/cba-yaafe-extension/blob/master/FEATURES.md)*.

## Installation

Before installing this extension, you have to install [YAAFE](http://yaafe.sourceforge.net)!

* Download the package and unzip
* <code>mkdir build</code>
* <code>cd build</code>
* <code>ccmake ..</code> type 'c' for configure and 'g' for generate
* <code>make</code>
* <code>sudo make install</code>

## Run

either use the **standard YAAFE-script** to extract the new features:

<code>yaafe.py -r 11025 --resample -f "cfa: ContinuousFrequencyActivation" wavefile.wav</code>

or use the **adapted one** to get the output directly to the commandline as **JSON-encoded** string:

<code>yaafe_cba.py -r 11025 --resample -f "cfa: ContinuousFrequencyActivation" wavefile.wav</code>

## License

The CBA-extension for YAAFE is released under GNU-LGPL v3.

## Contact

For questions, comments and complaints please use Issues on GitHub.

**Media Computing Research Group** (<http://mc.fhstp.ac.at>)  
Institute for Creative Media Technologies (IC\M/T)  
University of Applied Sciences St. Pölten (<http://www.fhstp.ac.at>)