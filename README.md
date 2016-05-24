# fusionkit
=================
FusionKit is a software suite developed by the Institute of Media Informatics / Ulm University within the EC-funded INTERACT project. It aims to be a low-cost tracking system based on multiple Kinect v2 time-of-flight cameras, which enables markerless body tracking as well as marker-based object tracking for a broad range of HCI and tracking scenarios. The toolkit is to be released as fully open source software and can be used and modified by industry, researchers and other groups interested in an easy-to-setup, affordable tracking solution.

For the time being, only binaries will be provided for download, as licensing issues still prevent us from releasing the source code publicly.

#License (for the provided binaries)
====================================
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE. BINARIES OF THIS SOFTWARE MAY NOT BE REDISTRIBUTED COMMERCIALLY OR NON-COMMERCIALLY, NOR MADE AVAILABLE TO ANY THIRD PARTY THROUGH ANY OTHER MEANS BESIDES DIRECT DOWNLOADS FROM THIS WEB PAGE.

#FAQ
=================================
## SensorServer system requirements
Windows 8 or greater, USB 3.0 port, Ethernet interface, i3 or greater CPU recommended.

## Studio system requirements
Windows 7 or greater, standalone GPU, CPU ressources depend on the number of cameras connected (i5 should work for a few cameras).

## How do I get started with this software?
Please see the getting started guide in the doc folder of the repository. A more detailed documentation will follow soon.

## I have problems starting the SensorServer or Studio Application
Please try to run the application with administrative rights.

## I have problems using the sensor discovery
Please make sure that you have a correct and complete network configuration. If you use an isolated network, please enter a gateway IP on all of the Sensor nodes and Studio node (the gateway does not need to exist, but the address has to be configured). Please also make sure that you allow the Sensor and Studio applications in the Windows-internal and/or any third-party firewall applications.

## I have problems with poor tracking quality
Before you start the registration process, it is crucial to select an appropriate sensor as main sensor (right click in the sensor list). The main sensor should have the biggest possible common space with all other sensors.

## I've encountered bugs or unexpected behaviour
Please note that this software is still in an early stage of development. Nonetheless, if you want to support further development and help us to recognize and fix any bugs that may be included, please use the GitHub issue tracking system of this project to describe the issue you encountered. 
