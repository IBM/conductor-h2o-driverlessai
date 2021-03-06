# conductor-h2o-driverlessai

To use Driverless AI with IBM Spectrum Conductor you need to download and install Driverless AI on each node of the cluster you plan to run Driverless AI. First download the TAR SH version to install on each host: https://s3.amazonaws.com/artifacts.h2o.ai/releases/ai/h2o/dai/rel-1.8.7-29/index.html

After installing Driverless AI on each host there is a folder with the name spectrum_conductor in the installation with an Application Template for having it run in IBM Spectrum Conductor. Download dai_template.yaml to your local computer. If you want to use Driverless AI with GPUs in IBM Spectrum Conductor use the Application Template in this git repo named dai_gpu_template.yaml.

Connect to the Conductor WEBGUI to register the application instance with the application template. For full details on registering an application template see: https://www.ibm.com/support/knowledgecenter/SSZU2E_2.4.1/manage_app_instances/app_instances_register.html 

Driverless AI allows all configurations to be specified as environment variables. When registering the application instance you can set the additional configuration to be a list separated by semi colon of parameters you want to set for the Additional Configuration parameter. Example: DRIVERLESS_AI_ENABLE_BENCHMARK=true;DRIVERLESS_AI_DATA_PRECISION=float32

The install directory is the full path directory created by the Driverless AI installer, example: /var/dai/dai-1.8.7-linux-x86_64

