#Sole-tenant nodes

- Sole-tenancy lets you have exclusive access to a sole-tenant node, which is a physical Compute Engine server 
that is dedicated to hosting only your project's VMs. Use sole-tenant nodes to keep your VMs physically separated from VMs in other projects, 
or to group your VMs together on the same host hardware, as shown in the following diagram.

- VMs running on sole-tenant nodes can use the same Compute Engine features as other VMs, including transparent scheduling and block storage, 
but with an added layer of hardware isolation. To give you full control over the VMs on the physical server, each sole-tenant node maintains 
a one-to-one mapping to the physical server that is backing the node.
