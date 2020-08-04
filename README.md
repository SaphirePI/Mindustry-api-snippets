# Mindustry-api-snippets

Get all players from the server, `import mindustry.Vars;`

```java
Vars.playerGroup.all()
```

Connect player to another server

```java
Call.onConnect(player.con, 'https://aspire.su', 6567);

// Hub trick
if (player.x <= 306 && player.x >= 263 && player.y >= 488 && player.y <= 531) { // Check if player joined inside this zone
    Vars.net.pingHost('https://aspire.su', 6567), host -> {
        Call.onConnect(player.con, 'https://aspire.su', 6567);
    }, e -> {
    });
}
```

Get player by num

```java
Player pl = Vars.playerGroup.all().get(id);
```


Show the label on the map

```java
Call.onLabel(event.player.con, 'Your text here', 1100f, 284f, 304f);
Call.onLabel('Your text here', 1100f, 284f, 304f);

```
