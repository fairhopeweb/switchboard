# Installation

## Impatient? On OS X? Install from binary tarball.

To quickly get Switchboard up and running on Mac OS X, you can use a prebuilt
release. If you want to do a quick install (I recommend verifying the contents
of the URL):

    curl URL | tar -xz && ./switchboard/_rel/bin/switchboard start

TODO md5

Because you won't be building the application, the client section of
[getting started](getting-started.md) will probably be most interesting
to you. Check out the Example Client section for directions on how to
connect a client.


## From Source

Switchboard uses `extend/erlang.mk` and `erlware/relx` to build and
package the application.

Switchboard depends on `make`, and Erlang/OTP R16B03. I'll leave
installing `make` up to you, but to install Erlang you can use
Homebrew if you're on Mac OS X, else check
[here](https://www.erlang-solutions.com/downloads/download-erlang-otp)
for the appropriate package/architecture and installation
instructions.

Now you can clone the project, build the application, package it into
a release, and start it.

	git clone https://bitbucket.org/thusfresh/imapswitchboard switchboard
	cd switchboard
	# Make the release
	make
	# Start the application
	./_rel/bin/switchboard start
	# Check whether the application is running
	./_rel/bin/switchboard ping  # -> ping

	# Print more options, like stopping Switchboard
	./_rel/bin/switchboard

Please create an issue if there were any problems!

Next, check out the [getting started pages](getting-started.md) to get you hacking.