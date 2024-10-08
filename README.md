# 12 Factor Apps methodology SaaS # – (CDCB BPPC DDLA)
**Codebase**: Maintain a single codebase tracked in version control. Multiple deployments of the same app should use the same codebase.<br />
**Dependencies**: Explicitly declare and isolate dependencies. Use a dependency management system to keep track of libraries (use maven).<br />
**Config**: Store configuration settings in the environment, separate from the code. Same code can be deployed across different environments.<br />
**Backing Services**: Treat backing services (databases, caches, etc.) as attached resources. Connect to these services via URLs or connection strings.<br />
**Build, Release, Run**: Keep these stages distinct. Builds create deployable, Releases combine these with configuration, and Runs execute the app. <br />
**Processes**: Run the app as one or more stateless processes. This enhances scalability, resilience, and ease of replacement. (Run in Containerize)<br />
**Port Binding**: For portability and scalability, assigning a port number to a process so that it can be accessed by other processes on the network.<br />
**Concurrency**: Is achieved by running multiple isolated (dif DB) and coordinated processes to handle multiple requests at same time via Queue, LB.<br />
**Disposability**: Max robustness with fast startup and graceful shutdown. Apps – should start and stop quickly, allowing for easy scaling and updates.<br />
**Dev/Prod Parity**: Keep dev, stage and prod env as similar as possible. Minimize differences to reduce the probability of issues arising in production.<br />
**Logs**: Treat logs as event streams and make them easily accessible. Log important events and errors to aid in debugging and monitoring.<br />
**Admin Processes**: Run admin tasks as one-off processes. Provide mechanisms for executing Mgt tasks, separate but keep in same codebase.<br />
