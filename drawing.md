flowchart LR
    subgraph Insecure_QP["Insecure QP"]
        A[VM1: RDMA Memory Region]
        B[VM2: Hacker]
        A -->|Steal 50 GB/s| B
    end

    subgraph Secure_QP["Secure QP"]
        C[VM1: RDMA Memory Region]
        D[Lock 🔒]
        E[VM2: Unauthorized Access Blocked]
        C --> D --> E
    end

    style Insecure_QP fill:#ffe5e5,stroke:#ff0000,stroke-width:2px
    style Secure_QP fill:#e0ffe0,stroke:#00aa00,stroke-width:2px
