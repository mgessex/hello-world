```mermaid
flowchart LR
    subgraph Public Internet
        User
    end
    subgraph LoadBalancingZone
        LoadBalancer
    end
    subgraph WebServerZone
        WebServerA
        WebServerB
    end

    User -- tcp/80--> LoadBalancer
    LoadBalancer --tcp/1337--> WebServerA
    LoadBalancer --tcp/1337--> WebServerB

    WebServerA --> DatabaseServerA
    WebServerB --> DatabaseServerA
    WebServerA -.-> DatabaseServerB
    WebServerB -.-> DatabaseServerB