<img src="{{ 'images/v21.2/ui_cpu_percent.png' | relative_url }}" alt="DB Console CPU Percent graph" style="border:1px solid #eee;max-width:100%" />

{{site.data.alerts.callout_info}}
This graph shows the CPU consumption by the CockroachDB process only and is useful as long as there are no other processes consuming significant CPU on the node. In case you have other processes running on the node, use a separate monitoring tool to measure the total CPU consumption across all processes.
{{site.data.alerts.end}}

- In the node view, the graph shows the percentage of CPU in use by the CockroachDB process for the selected node.

- In the cluster view, the graph shows the percentage of CPU in use by the CockroachDB process across all nodes.

{{site.data.alerts.callout_info}}
For multi-core systems, the percentage of CPU usage is calculated by normalizing the CPU usage across all cores, whereby 100% utilization indicates that all cores are fully utilized.
{{site.data.alerts.end}}