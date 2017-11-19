
# WARNING

DCCute should be considered alpha quality software at this time.  Although it works, it has not
been tested with any commercial DCC system. It has only been tested with DCC++ on an Arduino Uno.
The author of DCCute claims no responsibility or liability for any damage to your system,
equipment or trains.

__USE AT YOUR OWN RISK.__


# Summary

DCCute (pronounced D C Cute) is a lightweight remote control interface for model
railroads utilizing a DCC control system.  It's purpose is to allow the user to
test their DCC++ system quickly. It's keyboard based interface also allows the
user to quickly control multiple locomotives and decoders.

Screenshot of DCCute
![Screenshot of DCCute](http://suso.suso.org/images/dccute.png "Screenshot of DCCute")


# License

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public
License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see <http://www.gnu.org/licenses/>.

# Installation

DCCute is written for python3 and so far uses modules that come with
a standard python installation. dccute is meant to be lightweight and requires
a minimal install. You can either run `dccute` directly from the directory where
you downloaded it:

* `./dccute`

Or you can copy it to someplace in your `$PATH` so that you can run it without the
./ prefix.

# Configuration

Currently there is no configuration file or interface to setup your locomotives.
To configure your locomotives, find the comment "Define your locomotives" in the
dccute program code. There you will see a variable called _decoders_ that contains
two default locomotives on address 3 and 4 followed by their name. You can change,
remove or add to this list as needed.

# Running

DCCute is currently written to only work with [DCC++](https://github.com/DccPlusPlus/BaseStation)
running on an Arduino Uno, Mega or similar platform and listening on a
serial port such as `/dev/ttyACM0`.

When you start dccute, pass it one argument that is the path to the serial port that
your Arduino is listening on. For example:

`dccute /dev/ttyACM0`


# Interface

The interface is currently in development so please don't become too comfortable with
the way it works now. It may change.

Once you've started, power on the main track by pressing `p` on your keyboard. If it doesn't
work the first time you may have to press it a couple times. Select your locomotive from the on
screen list by pressing `1` - `9`. Use up arrow and down arrow to increase or decrease your throttle.
Left and right arrow change direction. Use F1 - F20 on your keyboard (F11 - F20
are accessed using SHIFT F1, F2, etc) to access decoder functions. I don't know of a
way to create function keys 21 - 28.

Press `q` or `Ctrl-C` to quit.

Currently I have the following keys assigned to function keys for effects on the decoder I use (SoundTraxx Econami Diesel)

* l - F0 - Lights
* b - F1 - Bell
* h - F2 - Horn
* H - F3 - Short horn
* d - F7 - Dimmer
* m - F8 - Mute
* c - F13 - Couple/Uncouple
* a - F23 - "All Aboard"

These may or may not correspond with the the same effects on decoders you use.


# Future plans

* Online configuration system. Allow creation and configuration of locomotives in the program.
* Allow unlimited decoders.
* Allow for other types of decoders such as switches.
* Configuration is saved on exit.
* Read in manufacturer decoder defaults from somewhere.
* Modularize Serial interface to allow plugging into other types of DCC control systems.

