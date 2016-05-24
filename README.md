# fusionkit
FusionKit is a software suite developed by the Institute of Media Informatics / Ulm University within the EC-funded INTERACT project. It aims to be a low-cost tracking system based on multiple Kinect v2 time-of-flight cameras, which enables markerless body tracking as well as marker-based object tracking for a broad range of HCI and tracking scenarios. The toolkit is to be released as fully open source software and can be used and modified by industry, researchers and other groups interested in an easy-to-setup, affordable tracking solution.

For the time being, only binaries will be provided for download, as licensing issues still prevent us from releasing the source code publicly.

#License (for the provided binaries)
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE. BINARIES OF THIS SOFTWARE MAY NOT BE REDISTRIBUTED COMMERCIALLY OR NON-COMMERCIALLY, NOR MADE AVAILABLE TO ANY THIRD PARTY THROUGH ANY OTHER MEANS BESIDES DIRECT DOWNLOADS FROM THIS WEB PAGE.

#Contact / Publications
For contact details, see http://uulm.de/?fusionkit

If you happen to use this software for any published research work, please cite our respective publications:
- Michael Rietzler, Florian Geiselhart, Janek Thomas and Enrico Rukzio
FusionKit: A Generic Toolkit for Skeleton, Marker and Rigid-Body Tracking
Proc. of the 8th ACM SIGCHI Symposium on Engineering Interactive Computing Systems (EICS 16)
- Florian Geiselhart, Michael Otto and Enrico Rukzio
On the use of Multi-Depth-Camera based Motion Tracking Systems in Production Planning Environments
In Proc. of CIRP CMS 2015 (48th CIRP Conference on Manufacturing Systems),

#FAQ

## System requirements
One Windows 7/8 machine for Studio (providing registration, fusion and skeleton output) with:
 - A decent CPU (i7 or better is recommended) 
 - .net Framework (>= 4.5.1)

One Windows 8 machine for each Kinect v2 sensor running the SensorServer, with:
- Suitable hardware for Kinect v2 tracking (i3 or greater, some GB of RAM, USB 3.0)
- .net Framework (>= 4.5.1)
- Kinect SDK v2.0
- Optional: CUDA SDK and supported GPU for accelerated marker tracking
- Network connections with sufficient throughput between all of the machines (isolated network without other traffic is preferred) and correct network configuration for UPnP/SSDP sensor discovery
 
The current version of the system has been tested with up to 8 sensors

## How do I get started with this software?
Please see the getting started guide below. A more detailed documentation will follow soon.

- Start up the StudioSensorServer binary on all sensor machines
- Start up the Studio binary on the Studio machine
- Add sensors by:
  - either using discovered sensors (hit "Refresh" if sensors are missing)
  - or add sensors manually by providing their IP address (button below sensor list on the left)
- Tick the checkboxes of all sensors to use them
- Start Registration Wizard on the Fusion Tab on the right side of the UI
- Follow the instructions provided by the Registration Wizard until quality is sufficient
- Switch skeleton display type for 3D view to view fused skeleton output
- The skeleton output data can also be polled using REST at <ip>:8083/frame

## I have problems starting the SensorServer or Studio Application
Please try to run the application with administrative rights.

## I have problems using the sensor discovery
Please make sure that you have a correct and complete network configuration. If you use an isolated network, please enter a gateway IP on all of the Sensor nodes and Studio node (the gateway does not need to exist, but the address has to be configured). Please also make sure that you allow the Sensor and Studio applications in the Windows-internal and/or any third-party firewall applications.

## I have problems with poor tracking quality
Before you start the registration process, it is crucial to select an appropriate sensor as main sensor (right click in the sensor list). The main sensor should have the biggest possible common space with all other sensors. Besides this, there are still a lot of factors which influence tracking quality (registration quality, occlusions, "ghost" skeletons, network performance and much more). If you have a specific scenario which you would expect to work, but which does not work, please contact us (see above) or create an issue here at GitHub.

## I've encountered bugs or unexpected behaviour
Please note that this software is still in an early stage of development. Nonetheless, if you want to support further development and help us to recognize and fix any bugs that may be included, please use the GitHub issue tracking system of this project to describe the issue you encountered. 
