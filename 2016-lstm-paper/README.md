Paper: [A Comprehensive Study of Deep Bidirectional LSTM RNNs for Acoustic Modeling in Speech Recognition](http://arxiv.org/abs/1606.06871),
authors: Albert Zeyer, Patrick Doetsch, Paul Voigtlaender, Ralf Schlüter, Hermann Ney.

This repo contains the configs,
to be used with [RETURNN](https://github.com/rwth-i6/returnn)
(called CRNN earlier/internally)
and [RASR](https://www-i6.informatik.rwth-aachen.de/rwth-asr/)
(called Sprint internally)
for data preprocessing and decoding.

Most experiments are for the Quaero 50h English corpus (see paper for details), we is private unfortunately.
Some experiments are for the Switchboard 300h English corpus but we also cannot publish the data ourselves.

To use the RETURNN configs with other data,
replace the `train`/`dev` config settings, which specify the train and dev corpus data.
At the moment, they will use the `ExternSprintDataset` interface to get the preprocessed data out of RASR.
You can also use other dataset implementations provided by RETURNN (see RETURNN doc / source code),
e.g. the HDF format directly.
