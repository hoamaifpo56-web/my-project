# 卵巢早衰(POI)治疗机制的信号网络通路图

```mermaid
flowchart TD
    A["卵巢早衰(POI)病因分类"] --> B
    B["不同病因POI的病理特征"] --> C
    C["核心信号枢纽网络"] --> D
    D["线粒体质量控制中心"] --> E
    E["细胞命运决策"] --> F
    F["卵巢功能恢复"]
    
    subgraph A["卵巢早衰(POI)病因分类"]
        A1[化学/药物诱导型] --> A11[环磷酰胺(CTX)]
        A11 --> A12[顺铂(Cisplatin)]
        A12 --> A13[其他化疗药物]
        A2[自身免疫型] --> A21[Zp3肽诱导]
        A21 --> A22[免疫细胞攻击]
        A3[衰老/衰退型] --> A31[D-半乳糖]
        A31 --> A32[自然衰老]
    end
    
    subgraph B["不同病因POI的病理特征"]
        B1[化学诱导型] --> B11[急性氧化应激]
        B11 --> B12[线粒体急性损伤]
        B12 --> B13[DNA损伤]
        B2[自身免疫型] --> B21[免疫炎症风暴]
        B21 --> B22[Treg/Th17失衡]
        B22 --> B23[NLRP3炎症小体激活]
        B3[衰老/衰退型] --> B31[慢性能量危机]
        B31 --> B32[自噬流受阻]
        B32 --> B33[干细胞衰竭]
    end
    
    subgraph C["核心信号枢纽网络"]
        C1["PI3K/AKT通路<br>主生存信号"] --> C11[激活mTOR]
        C2["AMPK/mTOR通路<br>能量/自噬开关"] --> C21[调节自噬平衡]
        C3["Hippo/YAP通路<br>细胞增殖/命运"] --> C31[促进组织再生]
        C4["Nrf2/HO-1通路<br>抗氧化防御"] --> C41[减轻氧化应激]
        
        C1 <--> C2
        C2 <--> C3
        C3 <--> C4
        C4 <--> C1
        
        C1 --> C5["mTOR信号整合中心<br>(生存/生长 vs. 自噬/存活)"]
        C2 --> C5
        C5 --> C6[线粒体质量控制]
    end
    
    subgraph D["线粒体质量控制中心"]
        D1[线粒体自噬] --> D11[PINK1/Parkin通路]
        D11 --> D12[BNIP3/NIX通路]
        D2[线粒体生物合成] --> D21[PGC-1α激活]
        D21 --> D22[TFAM上调]
        D3[抗氧化防御] --> D31[SOD/CAT/GPX4]
        
        D1 <--> D2
        D2 <--> D3
        D3 <--> D1
        
        D1 --> D4[线粒体功能恢复]
        D2 --> D4
        D3 --> D4
        
        D4 --> D41[线粒体膜电位恢复]
        D4 --> D42[ATP产生增加]
        D4 --> D43[ROS水平降低]
    end
    
    subgraph E["细胞命运决策"]
        E1[细胞凋亡] --> E11[Caspase-3激活]
        E11 --> E12[Bcl-2/Bax失衡]
        E2[细胞焦亡] --> E21[NLRP3/GSDMD]
        E3[铁死亡] --> E31[GPX4抑制]
        E31 --> E32[脂质过氧化]
        E4[细胞衰老] --> E41[SA-β-Gal阳性]
        E41 --> E42[p16/p21上调]
        
        E1 -.->|抑制| E5[颗粒细胞存活]
        E2 -.->|抑制| E5
        E3 -.->|抑制| E5
        E4 -.->|逆转| E5
        
        E5 --> E51[增殖能力恢复]
        E5 --> E52[激素合成增加]
        E5 --> E53[卵泡支持功能增强]
    end
    
    subgraph F["卵巢功能恢复"]
        F1[卵泡发育正常化] --> F11[原始卵泡库保存]
        F11 --> F12[窦卵泡数量增加]
        F2[激素水平恢复] --> F21[FSH水平降低]
        F21 --> F22[AMH/E2水平升高]
        F3[生殖功能改善] --> F31[排卵功能恢复]
        F31 --> F32[生育能力提高]
        F4[临床症状缓解] --> F41[月经周期恢复]
        F41 --> F42[更年期症状减轻]
    end
    
    G["干细胞/外泌体治疗"] --> C
    G --> D
    
    subgraph G["干细胞/外泌体治疗策略"]
        G1[天然干细胞/外泌体] --> G11[旁分泌效应]
        G11 --> G12[归巢能力]
        G2[预处理增强型] --> G21[缺氧预处理]
        G21 --> G22[热休克预处理]
        G22 --> G23[药物预处理(PQQ等)]
        G3[基因工程化型] --> G31[过表达miRNA]
        G31 --> G32[过表达功能蛋白]
        G4[先进递送系统] --> G41[水凝胶/支架]
        G41 --> G42[靶向纳米颗粒]
    end
    
    H["治疗作用机制"] --> I
    
    subgraph H["治疗作用机制"]
        H1[调节PI3K/AKT/mTOR通路]
        H2[平衡AMPK/mTOR信号]
        H3[激活Hippo/YAP通路]
        H4[增强Nrf2抗氧化通路]
        H5[直接调控线粒体质量控制]
    end
    
    subgraph I["核心科学问题"]
        I1["异病同治的分子基础"]
        I2[线粒体质量控制的核心枢纽地位]
        I3[信号网络的交叉对话与整合]
        I4[从通用治疗到精准医学]
    end

    style A fill:#ffe6e6
    style B fill:#e6f7ff
    style C fill:#fff2e6
    style D fill:#f0ffe6
    style E fill:#f9e6ff
    style F fill:#e6ffe6
    style G fill:#ffe6ff
    style H fill:#e6ffff
    style I fill:#ffffe6
    
    linkStyle 0 stroke:#ff6666,stroke-width:2px
    linkStyle 1 stroke:#6666ff,stroke-width:2px
    linkStyle 2 stroke:#cc66ff,stroke-width:2px
    linkStyle 3 stroke:#ffcc00,stroke-width:2px
    linkStyle 4 stroke:#66cc66,stroke-width:2px
    linkStyle 5 stroke:#ff9966,stroke-width:2px
    linkStyle 6 stroke:#3399ff,stroke-width:2px
    linkStyle 7 stroke:#9966ff,stroke-width:2px
```
