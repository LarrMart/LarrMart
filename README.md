flowchart TB
    classDef default display: flex, justify-content: center, padding: 32px, stroke-width: 0;
    classDef bgDark fill:#111, color: white, font-size: 20px, padding: 48px;
    classDef bgLight fill: lightgreen, color:#222, font-size: 20px, font-weight: bold;
    classDef trasl fill: transparent, stroke-width: 0;
    classDef sub color: white,margin: 32px, fill: white, stroke-width: 8px, stroke:#e8fceb, font-weight: bold, font-size: 24px;
    classDef proyect padding: 16px, fill: #e8fceb, display: flex, justify-content: center, align-items: center;

    subgraph PERSONAL-DATA
        direction LR
        rol((Front-end <br/> Developer)):::bgLight;
        name((Larroca<br />Martínez<br>Guillermo<br>Alejandro)):::bgDark;
        goal((Write clear, efficient<br /> and minimalistic code. <br/> Create enjoyable, and user-friendly <br/>digital products.)):::bgLight;
        
        rol --- |Role| name
        name --- |Goal| goal
    end

    subgraph PROYECTS
        direction TB
        PROJECTS(PROJECTS)
        subgraph PORTFOLIO
            direction TB
            proyect1(PORTFOLIO)
            description1(How to gather and showcase my projects in a unique way? <br />This question led to the creation of LMGA, the new operating system <br /> set to replace Windows in the near future...);
            tech1(EJS, SASS, JS, RollJS, NodeJS, HTML5 CANVAS);
            proyect1 -- description --> description1
            description1 -- tools --> tech1;
        end

        subgraph INVADERS
            direction TB
            proyect2(Invaders)
            description2(An enhanced and more entertaining remake of the classic 70s game.)
            tech2(HTML5 CANVAS, JS, HTML, CSS, RollUp JS, NodeJS)
            proyect2 -- description --> description2
            description2 -- tools --> tech2 
        end
    end

    PROJECTS --> PORTFOLIO
    PROJECTS --> INVADERS
    PERSONAL-DATA:::sub --> PROYECTS:::sub

class PROYECTS,PORTFOLIO,INVADERS sub;
class PROJECTS,proyect1,description1,tech1,proyect2,description2,tech2 proyect;
