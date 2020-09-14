# Shortcut Learning in Deep Neural Networks

## Summary

DNNs achieve
super-human performance recognising objects, but even small invisible changes [8] or a
different background context [9, 10] can completely derail predictions. DNNs can generate
a plausible caption for an image, but—worryingly—they can do so without ever looking
at that image [11]. DNNs can accurately recognise faces, but they show high error rates
for faces from minority groups [12]. DNNs can predict hiring decisions on the basis of
resum ´ es, but the algorithm’s decisions are biased towards selecting men [13].

While superficially successful, these strategies typically fail under slightly different circumstances. For instance, a DNN may appear
to classify cows perfectly well—but fails when tested on pictures where cows appear outside the typical grass landscape, revealing “grass” as an unintended (shortcut) predictor
for “cow”.

**Here shortcut means only with a pattern, model determines the prediction for an input, but this is not what we are expecting.**

In addition
to shortcut opportunities that are fairly easy to recognise, deep learning has led to the discovery of much more subtle shortcut features, including high-frequency patterns that are
almost invisible to the human eye [32, 33]. Whether easy to recognise or hard to detect,
it is becoming more and more evident that shortcut opportunities are by no means disappearing when the size of a dataset is simply scaled up by some orders of magnitude (in the
hope that this is sufficient to sample the diverse world that we live in
