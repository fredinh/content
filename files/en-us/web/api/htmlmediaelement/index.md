---
title: HTMLMediaElement
slug: Web/API/HTMLMediaElement
page-type: web-api-interface
tags:
  - API
  - Audio
  - HTML
  - HTML DOM
  - HTMLMediaElement
  - Interface
  - Media
  - Reference
  - Video
browser-compat: api.HTMLMediaElement
---
{{APIRef("HTML DOM")}}

The **`HTMLMediaElement`** interface adds to {{domxref("HTMLElement")}} the properties and methods needed to support basic media-related capabilities that are common to audio and video.

The {{domxref("HTMLVideoElement")}} and {{domxref("HTMLAudioElement")}} elements both inherit this interface.

{{InheritanceDiagram}}

## Properties

_This interface also inherits properties from its ancestors {{domxref("HTMLElement")}}, {{domxref("Element")}}, {{domxref("Node")}}, and {{domxref("EventTarget")}}._

- {{domxref("HTMLMediaElement.audioTracks")}}
  - : A {{domxref("AudioTrackList")}} that lists the {{domxref("AudioTrack")}} objects contained in the element.
- {{domxref("HTMLMediaElement.autoplay")}}

  - : A boolean value that reflects the {{htmlattrxref("autoplay", "video")}} HTML attribute, indicating whether playback should automatically begin as soon as enough media is available to do so without interruption.

    > **Note:** Automatically playing audio when the user doesn't expect or desire it is a poor user experience and should be avoided in most cases, though there are exceptions. See the [Autoplay guide for media and Web Audio APIs](/en-US/docs/Web/Media/Autoplay_guide) for more information. Keep in mind that browsers may ignore autoplay requests, so you should ensure that your code isn't dependent on autoplay working.

- {{domxref("HTMLMediaElement.buffered")}} {{readonlyinline}}
  - : Returns a {{domxref("TimeRanges")}} object that indicates the ranges of the media source that the browser has buffered (if any) at the moment the `buffered` property is accessed.
- {{domxref("HTMLMediaElement.controls")}}
  - : A {{jsxref('Boolean')}} that reflects the {{htmlattrxref("controls", "video")}} HTML attribute, indicating whether user interface items for controlling the resource should be displayed.
- {{domxref("HTMLMediaElement.controlsList")}} {{readonlyinline}}
  - : Returns a {{domxref("DOMTokenList")}} that helps the user agent select what controls to show on the media element whenever the user agent shows its own set of controls. The `DOMTokenList` takes one or more of three possible values: `nodownload`, `nofullscreen`, and `noremoteplayback`.
- {{domxref("HTMLMediaElement.crossOrigin")}}
  - : A string indicating the [CORS setting](/en-US/docs/Web/HTML/Attributes/crossorigin) for this media element.
- {{domxref("HTMLMediaElement.currentSrc")}} {{readonlyinline}}
  - : Returns a string with the absolute URL of the chosen media resource.
- {{domxref("HTMLMediaElement.currentTime")}}
  - : A double-precision floating-point value indicating the current playback time in seconds; if the media has not started to play and has not been seeked, this value is the media's initial playback time. Setting this value seeks the media to the new time. The time is specified relative to the media's timeline.
- {{domxref("HTMLMediaElement.defaultMuted")}}
  - : A {{jsxref('Boolean')}} that reflects the {{htmlattrxref("muted", "video")}} HTML attribute, which indicates whether the media element's audio output should be muted by default.
- {{domxref("HTMLMediaElement.defaultPlaybackRate")}}
  - : A `double` indicating the default playback rate for the media.
- {{domxref("HTMLMediaElement.disableRemotePlayback")}}
  - : A {{jsxref('Boolean')}} that sets or returns the remote playback state, indicating whether the media element is allowed to have a remote playback UI.
- {{domxref("HTMLMediaElement.duration")}} {{readonlyinline}}
  - : A read-only double-precision floating-point value indicating the total duration of the media in seconds. If no media data is available, the returned value is `NaN`. If the media is of indefinite length (such as streamed live media, a WebRTC call's media, or similar), the value is `+Infinity`.
- {{domxref("HTMLMediaElement.ended")}} {{readonlyinline}}
  - : Returns a {{jsxref('Boolean')}} that indicates whether the media element has finished playing.
- {{domxref("HTMLMediaElement.error")}} {{readonlyinline}}
  - : Returns a {{domxref("MediaError")}} object for the most recent error, or `null` if there has not been an error.
- {{domxref("HTMLMediaElement.loop")}}
  - : A {{jsxref('Boolean')}} that reflects the {{htmlattrxref("loop", "video")}} HTML attribute, which indicates whether the media element should start over when it reaches the end.
- {{domxref("HTMLMediaElement.mediaKeys")}} {{readonlyinline}} {{experimental_inline}}
  - : Returns a {{domxref("MediaKeys")}} object or `null`. MediaKeys is a set of keys that an associated HTMLMediaElement can use for decryption of media data during playback.
- {{domxref("HTMLMediaElement.muted")}}
  - : A {{jsxref('Boolean')}} that determines whether audio is muted. `true` if the audio is muted and `false` otherwise.
- {{domxref("HTMLMediaElement.networkState")}} {{readonlyinline}}
  - : Returns a `unsigned short` (enumeration) indicating the current state of fetching the media over the network.
- {{domxref("HTMLMediaElement.paused")}} {{readonlyinline}}
  - : Returns a {{jsxref('Boolean')}} that indicates whether the media element is paused.
- {{domxref("HTMLMediaElement.playbackRate")}}
  - : A `double` that indicates the rate at which the media is being played back.
- {{domxref("HTMLMediaElement.played")}} {{readonlyinline}}
  - : Returns a {{domxref('TimeRanges')}} object that contains the ranges of the media source that the browser has played, if any.
- {{domxref("HTMLMediaElement.preload")}}
  - : A string that reflects the {{htmlattrxref("preload", "video")}} HTML attribute, indicating what data should be preloaded, if any. Possible values are: `none`, `metadata`, `auto`.
- {{domxref("HTMLMediaElement.preservesPitch")}}
  - : A boolean value that determines if the pitch of the sound will be preserved. If set to `false`, the pitch will adjust to the speed of the audio.
- {{domxref("HTMLMediaElement.readyState")}} {{readonlyinline}}
  - : Returns a `unsigned short` (enumeration) indicating the readiness state of the media.
- {{domxref("HTMLMediaElement.seekable")}} {{readonlyinline}}
  - : Returns a {{domxref('TimeRanges')}} object that contains the time ranges that the user is able to seek to, if any.
- {{domxref("HTMLMediaElement.seeking")}} {{readonlyinline}}
  - : Returns a {{jsxref('Boolean')}} that indicates whether the media is in the process of seeking to a new position.
- {{domxref("HTMLMediaElement.sinkId")}} {{readonlyinline}} {{experimental_inline}}
  - : Returns a string that is the unique ID of the audio device delivering output, or an empty string if it is using the user agent default. This ID should be one of the `MediaDeviceInfo.deviceid` values returned from {{domxref("MediaDevices.enumerateDevices()")}}, `id-multimedia`, or `id-communications`.
- {{domxref("HTMLMediaElement.src")}}
  - : A string that reflects the {{htmlattrxref("src", "video")}} HTML attribute, which contains the URL of a media resource to use.
- {{domxref("HTMLMediaElement.srcObject")}}
  - : A {{domxref('MediaStream')}} representing the media to play or that has played in the current `HTMLMediaElement`, or `null` if not assigned.
- {{domxref("HTMLMediaElement.textTracks")}} {{readonlyinline}}
  - : Returns a {{domxref('TextTrackList')}} object containing the list of {{domxref("TextTrack")}} objects contained in the element.
- {{domxref("HTMLMediaElement.videoTracks")}} {{readonlyinline}}
  - : Returns a {{domxref('VideoTrackList')}} object containing the list of {{domxref("VideoTrack")}} objects contained in the element.
- {{domxref("HTMLMediaElement.volume")}}
  - : A `double` indicating the audio volume, from 0.0 (silent) to 1.0 (loudest).

### Event handlers

- {{domxref("HTMLMediaElement.onencrypted")}}
  - : Sets the event handler called when the media is encrypted.
- {{domxref("HTMLMediaElement.onwaitingforkey")}}
  - : Sets the event handler called when playback is blocked while waiting for an encryption key.

## Obsolete properties

These properties are obsolete and should not be used, even if a browser still supports them.

- {{domxref("HTMLMediaElement.controller")}} {{deprecated_inline}}
  - : A {{domxref("MediaController")}} object that represents the media controller assigned to the element, or `null` if none is assigned.
- {{domxref("HTMLMediaElement.mediaGroup")}} {{deprecated_inline}}
  - : A string that reflects the {{ htmlattrxref("mediagroup", "video")}} HTML attribute, which indicates the name of the group of elements it belongs to. A group of media elements shares a common {{domxref('MediaController')}}.
- {{domxref("HTMLMediaElement.mozAudioCaptured")}} {{readonlyinline}} {{non-standard_inline}} {{deprecated_inline}}
  - : Returns a {{jsxref('Boolean')}}. Related to audio stream capture.
- {{domxref("HTMLMediaElement.mozFragmentEnd")}} {{non-standard_inline}} {{deprecated_inline}}
  - : A `double` that provides access to the fragment end time if the media element has a fragment URI for `currentSrc`, otherwise it is equal to the media duration.

## Methods

_This interface also inherits methods from its ancestors {{domxref("HTMLElement")}}, {{domxref("Element")}}, {{domxref("Node")}}, and {{domxref("EventTarget")}}._

- {{domxref("HTMLMediaElement.addTextTrack()")}}
  - : Adds a new {{domxref("TextTrack")}} object (such as a track for subtitles) to a media element. This is a programmatic interface only and does not affect the DOM.
- {{domxref("HTMLMediaElement.captureStream()")}} {{experimental_inline}}
  - : Returns {{domxref("MediaStream")}}, captures a stream of the media content.
- {{domxref("HTMLMediaElement.canPlayType()")}}
  - : Given a string specifying a MIME media type (potentially with the [`codecs` parameter](/en-US/docs/Web/Media/Formats/codecs_parameter) included), `canPlayType()` returns the string `probably` if the media should be playable, `maybe` if there's not enough information to determine whether the media will play or not, or an empty string if the media cannot be played.
- {{domxref("HTMLMediaElement.fastSeek()")}} {{experimental_inline}}
  - : Quickly seeks to the given time with low precision.
- {{domxref("HTMLMediaElement.load()")}}
  - : Resets the media to the beginning and selects the best available source from the sources provided using the {{htmlattrxref("src", "video")}} attribute or the {{HTMLElement("source")}} element.
- {{domxref("HTMLMediaElement.pause()")}}
  - : Pauses the media playback.
- {{domxref("HTMLMediaElement.play()")}}
  - : Begins playback of the media.
- {{domxref("HTMLMediaElement.seekToNextFrame()")}} {{non-standard_inline}} {{experimental_inline}} {{deprecated_inline}}
  - : Seeks to the next frame in the media. This non-standard, experimental method makes it possible to manually drive reading and rendering of media at a custom speed, or to move through the media frame-by-frame to perform filtering or other operations.
- {{domxref("HTMLMediaElement.setMediaKeys()")}} {{experimental_inline}}
  - : Returns {{jsxref("Promise")}}. Sets the {{domxref("MediaKeys")}} keys to use when decrypting media during playback.
- {{domxref("HTMLMediaElement.setSinkId()")}} {{experimental_inline}}
  - : Sets the ID of the audio device to use for output and returns a {{jsxref("Promise")}}. This only works when the application is authorized to use the specified device.

## Obsolete methods

_These methods are obsolete and should not be used, even if a browser still supports them._

- {{domxref("HTMLMediaElement.mozCaptureStream()")}} {{non-standard_inline}}
  - : \[enter description]
- {{domxref("HTMLMediaElement.mozCaptureStreamUntilEnded()")}} {{non-standard_inline}} {{deprecated_inline}}
  - : \[enter description]
- {{domxref("HTMLMediaElement.mozGetMetadata()")}} {{non-standard_inline}} {{deprecated_inline}}
  - : Returns {{jsxref('Object')}}, which contains properties that represent metadata from the playing media resource as `{key: value}` pairs. A separate copy of the data is returned each time the method is called. This method must be called after the [loadedmetadata](/en-US/docs/Web/API/HTMLMediaElement/loadedmetadata_event) event fires.

## Events

_Inherits methods from its parent, {{domxref("HTMLElement")}}_ , defined in the {{domxref('GlobalEventHandlers')}} mixin. Listen to these events using [`addEventListener()`](/en-US/docs/Web/API/EventTarget/addEventListener) or by assigning an event listener to the `oneventname` property of this interface.

- {{domxref("HTMLMediaElement.abort_event", 'abort')}}
  - : Fired when the resource was not fully loaded, but not as the result of an error.
- {{domxref("HTMLMediaElement.canplay_event", 'canplay')}}
  - : Fired when the user agent can play the media, but estimates that **not** enough data has been loaded to play the media up to its end without having to stop for further buffering of content
- {{domxref("HTMLMediaElement.canplaythrough_event", 'canplaythrough')}}
  - : Fired when the user agent can play the media, and estimates that enough data has been loaded to play the media up to its end without having to stop for further buffering of content.
- {{domxref("HTMLMediaElement.durationchange_event", 'durationchange')}}
  - : Fired when the duration property has been updated.
- {{domxref("HTMLMediaElement.emptied_event", 'emptied')}}
  - : Fired when the media has become empty; for example, when the media has already been loaded (or partially loaded), and the {{domxref("HTMLMediaElement.load()")}} method is called to reload it.
- {{domxref("HTMLMediaElement.ended_event", 'ended')}}
  - : Fired when playback stops when end of the media (\<audio> or \<video>) is reached or because no further data is available.
- {{domxref("HTMLMediaElement.error_event", 'error')}}
  - : Fired when the resource could not be loaded due to an error.
- {{domxref("HTMLMediaElement.loadeddata_event", 'loadeddata')}}
  - : Fired when the first frame of the media has finished loading.
- {{domxref("HTMLMediaElement.loadedmetadata_event", 'loadedmetadata')}}
  - : Fired when the metadata has been loaded
- {{domxref("HTMLMediaElement.loadstart_event", 'loadstart')}}
  - : Fired when the browser has started to load a resource.
- {{domxref("HTMLMediaElement.pause_event", 'pause')}}
  - : Fired when a request to pause play is handled and the activity has entered its paused state, most commonly occurring when the media's {{domxref("HTMLMediaElement.pause()")}} method is called.
- {{domxref("HTMLMediaElement.play_event", 'play')}}
  - : Fired when the `paused` property is changed from `true` to `false`, as a result of the {{domxref("HTMLMediaElement.play()")}} method, or the `autoplay` attribute
- {{domxref("HTMLMediaElement.playing_event", "playing")}}
  - : Fired when playback is ready to start after having been paused or delayed due to lack of data
- {{domxref("HTMLMediaElement.progress_event", "progress")}}
  - : Fired periodically as the browser loads a resource.
- {{domxref("HTMLMediaElement.ratechange_event", 'ratechange')}}
  - : Fired when the playback rate has changed.
- {{domxref("HTMLMediaElement.resize_event", 'resize ')}}
  - : Fired when one or both of the `videoWidth` and `videoHeight` properties have just been updated.
- {{domxref("HTMLMediaElement.seeked_event", 'seeked ')}}
  - : Fired when a seek operation completes
- {{domxref("HTMLMediaElement.seeking_event", 'seeking')}}
  - : Fired when a seek operation begins
- {{domxref("HTMLMediaElement.stalled_event", 'stalled')}}
  - : Fired when the user agent is trying to fetch media data, but data is unexpectedly not forthcoming.
- {{domxref("HTMLMediaElement.suspend_event", 'suspend')}}
  - : Fired when the media data loading has been suspended.
- {{domxref("HTMLMediaElement.timeupdate_event", 'timeupdate')}}
  - : Fired when the time indicated by the {{domxref("HTMLMediaElement.currentTime", "currentTime")}} property has been updated.
- {{domxref("HTMLMediaElement.volumechange_event", 'volumechange')}}
  - : Fired when the volume has changed.
- {{domxref("HTMLMediaElement.waiting_event", 'waiting')}}
  - : Fired when playback has stopped because of a temporary lack of data.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

### References

- {{HTMLElement("video")}} and {{HTMLElement("audio")}} HTML elements.
- {{domxref("HTMLVideoElement")}} and {{domxref("HTMLAudioElement")}} interfaces, derived from `HTMLMediaElement`.

### Guides

- [Web media technologies](/en-US/docs/Web/Media)
- Learning area: [Video and audio content](/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
- [Guide to media types and formats on the web](/en-US/docs/Web/Media/Formats)
- [Handling media support issues in web content](/en-US/docs/Web/Media/Formats/Support_issues)
