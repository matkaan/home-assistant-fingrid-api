# Home Assistant Fingrid API

Home Assistant sensor for Fingrid open API data.

## Sensors
Currently only one simple sensor:
- **fingrid-power-system-state** Can be used to e.g. ramp down home energy consumption (automatically or manually), when there is risk of electicity sortage. API variable ID: 209

## Usage
1. Register Fingrid API key, see https://data.fingrid.fi/fi/pages/api
2. Add API secret to your secrests.yaml -file: "fingrid_api_key: [your personal Fingrid api key]"
4. Add sensor code to configuration.yaml
5. Add entity to dashboard etc.

## UI example

'''
type: entities
entities:
  - entity: sensor.fingrid_power_system_state

type: history-graph
entities:
  - entity: sensor.fingrid_power_system_state
    name: Fingrid
'''

![Fingrid power status dashboard example!](/examples/haas-fingrid-power-status.jpg "Fingrid power status dashboard example")

## Links
- Fingrid open API https://api.fingrid.fi/ 
- Fingrdi API instructions: https://data.fingrid.fi/fi/pages/api
- Swagger https://data.fingrid.fi/open-data-api/#!/event-controller/getEventJsonUsingGET
- HAAS RESTfull sensor: https://www.home-assistant.io/integrations/rest/
