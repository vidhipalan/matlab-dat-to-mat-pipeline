# matlab-dat-to-mat-pipeline
Automation pipeline to convert .dat files into MATLAB-readable .mat format using Docker on Synology NAS.

Docker Command - sudo -S docker run -d \  
  --name Matlab_docker \
  --mac-address="xx:xx:xx:xx:xx:xx" \
  -v /matlablicense/license_docker.lic:/licenses/license.lic \
  -v /volume1/AI_Sole_test/Participant_Data/:/data:rw \
  -e MLM_LICENSE_FILE=/licenses/license.lic \
  --entrypoint bash \
  mathworks/matlab:r2025a \
  -c "tail -f /dev/null"
