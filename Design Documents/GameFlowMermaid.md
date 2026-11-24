```mermaid
flowchart TD

    MM[Main Menu]

  

    MM --> Play

    MM --> Options

    MM --> Credits

    MM --> Exit

  

    Options --> Video

    Options --> Audio

    Options --> Controls

  

    Play --> JoinGame[Join Game]

    Play --> HostGame[Host Game]

  

    JoinGame --> Lobby

    HostGame --> Lobby

  

    Lobby --> RoleSelect[Role Selection / Ready Up]

    RoleSelect --> Run

  

    Run --> Pause

  

    Pause --> Run

    Pause --> Options

    Pause --> MainMenu

  

    Run --> Results

  

    Results --> Lobby

    Results --> MainMenu

  

    Collection --> Characters

    Collection --> ShoppingCart

    Collection --> Cosmetics

    Collection --> Achievements

  

    Results --> Col[Collection Rewards]

    MM --> Collection
```