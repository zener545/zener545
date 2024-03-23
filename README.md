this code is not giving music information this code is belong to rain meter
any can slove this
- 👋 Hi, I’m @zener545
- 👀 I’[Rainmeter]
Update=1000
Author=Connect-R
BackgroundMode=2
SolidColor=0,0,0,1
DynamicWindowSize=1
AccurateText=1
MouseScrollUpAction=[!SetVariable Scale "(#Scale#+#ScrollMouseIncrement#)"][!WriteKeyValue Variables Scale "(#Scale#+#ScrollMouseIncrement#)"][!Refresh] 
MouseScrollDownAction=[!SetVariable Scale "(#Scale#-#ScrollMouseIncrement# < 0.2 ? 0.2 : #Scale#-#ScrollMouseIncrement#)"][!WriteKeyValue Variables Scale "(#Scale#-#ScrollMouseIncrement# < 0.2 ? 0.2 : #Scale#-#ScrollMouseIncrement#)"][!Refresh]

[Metadata]
Name=
Author=
Information=
License=
Version=


[Variables]
@include=#@#Variables.inc
@include2=#@#Language\Language.inc
Scale=0.5

;-------------------------------------------------------------
;-------------------------------------------------------------

[MeasureArtist]
Measure=Plugin
Plugin=NowPlaying.dll
PlayerName=Spotify
PlayerType=ARTIST

[MeasureTitle]
Measure=Plugin
Plugin=NowPlaying.dll
PlayerName=Spotify
PlayerType=TITLE

[MeasureDuration]
Measure=Plugin
Plugin=NowPlaying.dll
PlayerName=Spotify
PlayerType=DURATION

[MeasurePosition]
Measure=Plugin
Plugin=NowPlaying.dll
PlayerName=Spotify
PlayerType=POSITION

[MeasureMinutesRemaining]
Measure=Calc
Formula=Trunc((MeasureDuration - MeasurePosition)/60)
RegExpSubstitute=1
Substitute="^(.)$":"0\1"

[MeasureSecondsRemaining]
Measure=Calc
Formula=((MeasureDuration - MeasurePosition) % 60)
RegExpSubstitute=1
Substitute="^(.)$":"0\1"

;-------------------------------------------------------------
;-------------------------------------------------------------

[MeterArtistAndTitle]
Meter=String
MeasureName=MeasureArtist
MeasureName2=MeasureTitle
StringAlign=Center
FontFace=Helvetica 65 Medium
FontColor=White
FontSize=(25*#Scale#)
X=(280*#Scale#)
Y=(0*#Scale#)
W=(550*#Scale#)
Text="%1-%2"
ClipString=1
AntiAlias=1

[MeterRemaining]
Meter=String
MeasureName=MeasureMinutesRemaining
MeasureName2=MeasureSecondsRemaining
StringAlign=Center
FontFace=Helvetica 65 Medium
FontColor=White
FontSize=(20*#Scale#)
X=(0*#Scale#)r
Y=(5*#Scale#)R
Text="#Remaining# - %1:%2"
InlinePattern=#Remaining#
InlineSetting=Color | #Color1#
AntiAlias=1
m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
zener545/zener545 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
