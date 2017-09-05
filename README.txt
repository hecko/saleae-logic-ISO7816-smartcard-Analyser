This build assumes the SDK to be located on the same level as this checked out directory and be called

	AnalyzerSDK

You can checkout the AnalyzerSDK from https://github.com/saleae/AnalyzerSDK
Tested with master branch with latest commit on May 12, 2017

I norder to compile Windows version move the SDK files into
the following directories:
- ../sdk/include - for headers (*.hpp)
- ../sdk/lib     - for libraries

Files and Directories:

source
	Actual source code; including a simple Makefile.

ISO7816Analyser
	XCode build environment for above source.

VCProj
	VC2015 build environment for above source.

Licenses.txt
	License information.

README.txt
	This file
