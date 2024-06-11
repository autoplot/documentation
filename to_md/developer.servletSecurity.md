Purpose: outline new precautions to make servlets more secure.

Audience: Autoplot developers and data providers interested in using the
Autoplot servlet.

# The Problem

Though the servlet was first deployed a few years ago, not much
attention was paid to security, and because of this there are potential
holes that need to be patched up. For example, the servlet could be used
to make a plot of a local file, and then the image could be used to
recreate the file. Likewise, .jyds data sources could be used fairly
easily made to be hostile towards the server. For these reasons, the
servlet should still be considered experimental and should not be used.

# Solutions

Local vaps can be considered non-hostile. We need to keep in mind that
there may be ways to introduce a vap onto the server. For example, the
attacker could attempt to plot the remote vap, but then knowing that the
remote vap is now cached in the server's local cache, use a reference to
it to trick the servlet into thinking the resource is local. (This has
been handled.)

However, vaps from outside of the server must be considered hostile.
They must only contain references to data outside of the server. Also,
since .jyds files are run on the server, they must be assumed to be
hostile.

People that wish to serve their data in images alongside their digital
data can use "ro\_cache.txt" files within the servlet file cache so that
copies are not made.

# To Consider

Even if a vap is remote and all the references are remote, the server
could be made to download excessive resources, filling disks and
encumbering networks.
