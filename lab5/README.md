# Lab 5: AIS Vessel Movement Flow Map

## 1. Study Area and Dates
- Region Selected: Puget Sound and Seattle Region.
- Date Range: July 2, 2025 – July 4, 2025.
- Data Source: [AccessAIS - MarineCadastre.gov](https://marinecadastre.gov/accessais/)
- Dataset Management: To keep the dataset manageable in runtime while having enough data, I drew the spatial extent around the highly dense movement lanes around the Puget Sound region while keeping the collection range around a two day window. 
- Time Zone: The clock times and map interface controls are in local Pacific Daylight Time (PDT).


## 2. Interpretations & Patterns
- Overall Patterns: I found that the Passenger ferries had big activity spikes that alligned with regular commuting schedules, running between 05:30 PDT and 23:30 PDT between the Seattle, Bainbridge Island, and Bremerton areas. However, the passenger traffic dropped significantly overnight, while the other vessel types typically had steady, continuous movement all day/night.
- Passengers, Cargos, Tankers, and Other Vessels: 
  - Passenger: Ferries followed mainly east-west channels directly connecting Seattle with Bainbridge and surrounding areas.
  - Cargo & Tankers: Large commercial vessels adhered tightly to the north-south deep-water lanes in Puget Sound, making wide-radius turns near industrial docks in West Seattle and Tacoma.
  - Other Vessels: These vessels had super high spatial variation, frequently crossing primary channels and/or idling near coastlines.
- Category Insights: Filtering down to individual vessel types reveals that while cargo ships occupy the primary navigation channels, passenger vessels dictated frequent horizontal traffic across the main shipping lanes.

## 3. Feature Proposal for Potential Users
- Postential Users & Needs: Traffic safety analysts who needs to identify real-time route overlaps and velocity differences between high-speed passenger ferries and deep-draft cargo ships in narrow waterways.
- Informing Resource: [deck.gl Interactivity Guide](https://deck.gl/docs/developer-guide/interactivity)
- Proposed Feature: An interactive trajectory and speed panel. Hovering over or clicking any active vessel path would highlight the trajectory, display a dynamic tooltip with the vessel's name, MMSI, current speed, and open a historical speed profile chart in a side panel.
- Utility: This feature would allow safety coordinators to quickly analyze individual vessel behavior during incidents or speed-restricted zone violations without cluttering the main flow map.