Intro
=====

This package allows to quickly setup an osc server to communicate with [the muse headband](htttp://choosemuse.com). 
This is based on the example shown in the [dev site](https://sites.google.com/a/interaxon.ca/muse-developer-site/developer-getting-started-guide)

Usage:
```python
def myfunc(eeg):
    print eeg.TP9,eeg.FP1,eeg.FP2,eeg.TP10

muse=Muse(5000)
muse.register_callback(EEG,myfunc)
muse.start()
#do sth for waiting here
```

The list of available paths can be found in the [module itself](https://github.com/capitancambio/pyrnassus/blob/master/pyrnassus/pyrnassus.py#L33) (I'll put the real docs somewhere soon).
Some paths are configured to return objects instead of values from the underlying osc server, again the docs are missing but can have a look in the [code itself](https://github.com/capitancambio/pyrnassus/blob/master/pyrnassus/pyrnassus.py#L131)

TODO:
  * Add a method to be able to override the default data builders for custom calls.



