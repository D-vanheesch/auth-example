# Samenvatting

## Context

- createContext

Aanmaken van een context
Wat krijg je dan terug???

1. Provider gedeelte

Aan de provider geef je mee welke props (data, functies) je beschikbaar wil maken aan de rest van de App.

Vaak zet je tussen de Provider opening tag en sluit tag de "props.children", dat is de rest van de app aan wie je data wil doorgeven

Je "Wrapped" de App met de Provider

2. Consumer ( in dit voorbeeld niet gebruikt )

- useContext (haalt de data van de context uit het Consumer gedeelte)

Hook die de data uit een Context object haalt

Elke keer als data veranderd, worden de waarden automatische geupdate! (want het is een "hook")

- Custom hook (optioneel): useAuthState

Haalt de authState op uit de AuthContext

Geeft nog extra info mee:
isAuthenticated

returned all deze data, zodat je die in je component kan gebruiken

## Wat is useHistory

- Hook!
- useHistory in React component gebruiken
- Dan krijgen we iets terug ...
- history object
  - history.push() -> stuur de gebruiker naar een bepaalde pagina
  - history.goBack() -> stuur de gebruiker naar vorige pagina

## Zijn er verschillen tussen Controlled Components & React Form

- Verschillen

Controlled component:

Slaat de waarden van een input veld op in: State

```javascript
    value={username}
    onChange={(e) => setUsername(e.target.value)}
```

```javascript
  <form onSubmit={onSubmit}>
```

```javascript
async function onSubmit(event) {
    // Als je react-hook-form gebruikt hoeft dit niet, dat gebeurt dan automatisch
    event.preventDefault(); // zorg dat je pagina niet refreshed
```

Hookform:

Houdt de waarde bij voor je met de "useForm hook"

```javascript
ref = { register };
```

```javascript
    <form onSubmit={handleSubmit(onSubmit)}>
```

- Overeenkomsten

- name, id, type etc. altijd goed om toe te voegen (accesibility)
