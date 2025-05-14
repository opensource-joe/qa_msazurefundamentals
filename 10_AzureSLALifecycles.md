# Understanding Azure Service Level Agreements and Lifecycles

## Azure SLAs
- Details: What level of reliability or performance you can expect from a given service.
- Compensation: How you will be compensated if MS doesn't meet that level.
- Guarantee: Available uptime. Apps will be available 99.95% of the time. Calculated monthly.

- Azure Service Health - can track app outages and send alerts.
- Increase uptime guarantees - use SSD over HDD, have redundancy in same zones.

- SLAs based on Azure services.
- Does not apply when there is a customer error - bug, shut down service, and violate MS rules.

## Azure Service Lifecycle
- Adds and removes services on a predictable basis.
- Azure updates lists service updates and features. There are public and private previews. Previews not completely tested. Private previews need to be for registered users to become an official tester. Not a good idea to run production services on a preview.