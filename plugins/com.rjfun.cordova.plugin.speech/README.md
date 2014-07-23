# com.luhuiguo.cordova.speech

This plugin provides the ability to speech recognition and synthesis‎ (over iFlytek voicecloud) on a device.


## Installation

cordova plugin add com.luhuiguo.cordova.speech --variable IOS_APP_ID=*IOS_APP_ID* --variable ANDROID_APP_ID=*ANDROID_APP_ID*

### Attention
please replace the iFlytek SDK files(ios/iflyMSC.framework and android/libs) with the version for your app.

## Supported Platforms

* Android
* iOS

## Methods

    speech.addEventListener
    speech.removeEventListener

    speech.startListening
    speech.stopListening
    speech.cancelListening
    
    speech.startSpeaking
    speech.pauseSpeaking
    speech.resumeSpeaking
    speech.stopSpeaking

## Events
    
    SpeechBegin
    SpeechEnd
    SpeechCancel
    SpeechResults
    SpeechError  
    VolumeChanged

    SpeakBegin
    SpeakPaused
    SpeakResumed
    SpeakCancel
    SpeakCompleted 
    SpeakProgress
    BufferProgress

## Example

    navigator.speech.addEventListener('SpeechResults', function(e){
    	console.log('onSpeechResults:' + e.results);
    });

    navigator.speech.startListening();

    navigator.speech.startSpeaking('你好，语音合成');

