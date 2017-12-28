# EDI X12 270 Processing Example
This is a project that demonstrates processing an X12 270 message using MuleSoft Anypoint B2B. The project parses a 270 from a Provider and generates individual entity files in XML. Future version will include the 271 message from the Payer on subscriber or dependent eligibility.

## Application Flow

<img src="https://github.com/djuang1/mulesoft-edi-x12-270-processing/blob/master/assets/x12-270-input.png" width="200px">

<img src="https://github.com/djuang1/mulesoft-edi-x12-270-processing/blob/master/assets/x12-270-processing.png" width="500px">

## Setup
1. Download project and import into Anypoint Studio
2. Open <b>mule-app.properties</b> file
  * Configure properties for SFTP folder where you will upload the .edi file
  * Configure properties for the folder where you will drop the .edi file. The default locations are within the project itself.
3. Run project
4. Copy the .edi files from <b>src/main/resources</b> into the <b>in</b> folder
5. Navigate to the <b>out</b> folder to see the generated entities from the .edi file.

## Resources

- Anypoint B2B - https://docs.mulesoft.com/anypoint-b2b/
- Overview of EDI file <b>generic request by clinic for patient - 270 - 1.edi</b> - http://www.x12.org/examples/005010X279/subscriber-who-is-also-the-patient/generic-request-by-clinic-for-patient-(subscriber)-eligibility/
