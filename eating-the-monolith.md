# Eating the Monolith

1. It’s important to keep in mind that dependency direction should always go from inside of the monolith to 
outside of the monolith, and not the other way around, so we don’t end up in that distributed monolith situation. 
This means when extracting services out of the monolith, start with the core services and work your way out to
the feature level.
2. Look for gravitational pulls that keep developers working in the monolith. It’s common for shared tooling to 
be built over time that makes development inside the monolith very convenient. For example, feature flags at GitHub 
provide monolith developers peace of mind for having control over who sees a new feature as it goes from staff shipped 
to beta to production. Make these shared resources available to developers outside of the monolith and start shifting 
that gravitational pull.
3. remove old code paths once new services are up and running. Use a tool to understand who’s calling this service and
have a plan to move 100% of the traffic over to the new service

## ...so you don’t get stuck supporting two sets of code forever
