# SwedishGermanVoiceRecognition
Use machine learning to distinguish 10 second German and Swedign conversational .wav snippets (about one hundred samples of each language)

By taking spectrograms of the wav files and feeding them to a resnet CNN, the file fails to disntiguish Germans and Swedes
(i.e. languages that are in various respects quite similar) in about 25% of the validation sample (i.e. anywhere from 15% to as high as 30%, which I took as a sign that we need a larger dataset so as to obtian something that is more similar from run to run).

I tried various ways of improving the analysis -- cutting off the frequency range to say 4K (so as to allow the bottom "interesting" portions to predominate more of the visual area under consideration). This helped a bit.

I also tried dividing the spectrogram into several chunks (i.e. snippets of shorter duration), so as to allow the limited number of pixels to
focus in on smaller details, but this proved counterproductive.

I also added French to the language set, presuming that that language would be easier to distinguish.

Finally, I increased the sample size to 200.
