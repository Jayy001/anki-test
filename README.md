```mermaid
%%{
  init: {
    "sequence": {
      "actorFontFamily": "monospace",
      "actorFontWeight": "bold",
      "messageFontFamily": "monospace",
      "messageFontWeight": "bold",
      "noteFontWeight": "bolder"
    }
  }
}%%

sequenceDiagram
  autonumber
  participant Browser
  participant AppServer

  rect rgb(255, 255, 255, 0.05)
    note over Browser, AppServer: (Phase 1) Authentication Check

    Browser ->> AppServer: GET /admin { Cookie:  }
    Browser ->> Browser: useSession
  end
end
```
