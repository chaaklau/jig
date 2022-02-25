# Jig: Tone Language Visualization (v0.1)

This is a visualisation system designed for the teaching and learning of any tonal language. It takes segmented text and romanization as input, and displays the romanized form with a schematic display of the tones for each syllable, as a way to visualize tonal features by moving or rotating the text, or by color-coding the syllables. A common usage is to display syllables with a high tone above the baseline, low tones below the baseline and rising tones by tilting the text. 

## Demo

 Here is a demo of the system using Hong Kong Cantonese as an example. Two files need to be prepared in order to handle a language variety. A *Jig* (`profile/yue_HK_jig.json`) is a file that describes all tonemes (phonological tone categories), which specifies a list of possible tones, pitch height, phonation type, and a list of tone sandhis. A separate *Theme* (`themes/yue_HK_theme.json`) is needed to specify how the tone shall be schematically displayed, in particular the height, rotation and color for each tone and variants. 


## Language Specification

To be added.

## The handling of tonal allophones

A tone category may be pronounced in multiple ways depending on where it is in a word. This can be specified in the *Jig*. To be added.

