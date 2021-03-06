Comments about BROWSE

The Video I/O (VIO) system can be used in OS/2 to simplify presentation of
data on the screen.  Presentation Manger supports windowed text output with
its Advanced Video I/O (AVIO) system.

In the VBROWSE subdirectory, there is a simple file browser which
demonstrates the use of VIO calls.  This program works in fullscreen
and VIO Windowed OS/2 sessions.

The BROWSE.EXE in the AVBROWSE subdirectory is an extension of the VIO
Browser, which demonstrates the use of AVIO in Presentation Manager, and
techniques for converting a VIO application to an AVIO application.  In
addition acting like the VIO sample, this sample also has features for
font shrinking and enlarging fonts, and allows selection of files using the
OPENDLG File Open protocol.

With both programs you select the file you want to browse with the first
argument on the command line.  E.g., "browse browse.c" will allow you
to examine the source code.  You can also browse from stdin, which is most
useful for piping to the browser.  E.g., "cl prog1.c | browse" will allow you
to browse through error messages.

Also note that there are severe memory restrictions on the file being
browsed:  the limit is min( 64K of text , 4096 lines of text).	The number
of lines is limited by the constant NUM_DATA_LINES found in browse.h.
The size of the text area is limited to 64K by virtue of the c malloc()
function.

File List:

README		This file
BROWSE		Makes AVBROWSE, VBROWSE

In the VBROWSE directory (VIO Browsing utility)
BROWSE		Makefile
BROWSE.C	Browsing routines
BROWSE.DEF	Definition file
BROWSE.EXE	Executable
BROWSE.H	Header file
BROWSE.SYM	Symbol file

In the AVBROWSE directory (note--this uses the OPENDLG library)
AVIO.C		Avio C routines
AVIO.H		Avio headers
BROWSE		Makefile
BROWSE.C	Browse source file
BROWSE.DEF	Definition file
BROWSE.EXE	Executable file
BROWSE.H,	Header file (defines resource ids)
BROWSE.ICO	Icon
BROWSE.RC	Resources
BROWSE.SYM	Symbol file
