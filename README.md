# OctoPrint-PanTilt <command_handler feature branch>

This topic branch adds the abilty to register pantilt_handlers with the main PanTilt plugin for receipt of pan/tilt messages.

The receiver plugin needs to register plugin hook as seen below:

global __plugin_hooks__
	__plugin_hooks__ = {
		"octoprint.plugin.softwareupdate.check_config": __plugin_implementation__.get_update_information,
		"octoprint.plugin.pantilt_handler": __plugin_implementation__.handle_pantilt
	}

The main PanTilt plugin will then pass changes in the web cam controls to all registered handlers.  This lets each type
of pan/tilt camera implementation define the setup and interface with the hardware.

https://github.com/c-devine/OctoPrint-PanTilt/archive/command-handler.zip

**TODO:** Describe what your plugin does.

## Setup

Install via the bundled [Plugin Manager](https://github.com/foosel/OctoPrint/wiki/Plugin:-Plugin-Manager)
or manually using this URL:

    https://github.com/Salandora/OctoPrint-PanTilt/archive/master.zip

**TODO:** Describe how to install your plugin, if more needs to be done than just installing it via pip or through
the plugin manager.

## Configuration

**TODO:** Describe your plugin's configuration options (if any).
