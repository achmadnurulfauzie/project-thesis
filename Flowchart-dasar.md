## Flowchart for Gaussian Blur Image Processing with MPI

```mermaid
graph TD
    A((Start)) --> B(Validate arguments)
    B --> |Valid| C{Number of Tasks <br/> >= 2?}
    C --> |Yes| D[Load image <br/> Create result Mat <br/> Distribute rows]
    C --> |No| E[Exit program]
    D --> F(Process slices in parallel)
    F --> G[Collect slices from all processes]
    G --> H(Save result to file)
    H --> I((End))
    E --> I((End))
    
```
