# Non-Functional Requirements Draft

Basically based on the current one in the tex file.

- The web UI should be able to visualize the network topology and update the visualization based on real time data streams.
- The rendering latency should be no longer than 2 seconds.
- The web UI should be viewable on modern web browsers.
- The framework should be able to handle data streamed from at least *N* sensors. **(Have to ask Kushy lower bound of the sensors count we are going to handle)**
- The framework should be able to save data collected in a specified period of time.
- The web UI should be modular and easily extendable with:
  - New diagram types.
  - New filters and aggregation methods.
  - New data types for input data.
- The system needs to provide access control that authenticates users ~~by using user name and password~~. *(I think once we specify it's gonna be user name and password, it becomes a function requirement, right? ie. The system can authenticate users via user name and password.)*

*I think we should focus on the data viz instead of access control. We can just make a proof of concept one at first and allow 2 user privilege levels. So...*

- Users should be able to have different privilege/access levels.


