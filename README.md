*This project has been created as part of the 42 curriculum by login1, login2.*

# ft_irc

An IRC server implemented in C++98, built as part of the 42 curriculum.
Supports multiple simultaneous clients, channel management, and real-time messaging over TCP/IP.

## Build

```bash
make
```

## Usage

```bash
./ircserv <port> <password>
```

## Connecting

```
nc -C localhost <port>
```

Register with:

```
PASS <password>
NICK <nickname>
USER <username> * * :<realname>
```

## Commands

| Command | Description |
|---------|-------------|
| `PASS <password>` | Authenticate during registration |
| `NICK <nickname>` | Set or change nickname |
| `USER <username> * * :<realname>` | Set user information |
| `JOIN <channel>` | Join or create a channel |
| `PART <channel> [message]` | Leave a channel |
| `PRIVMSG <target> <message>` | Send a message to a user or channel |
| `KICK <channel> <nickname>` | Remove a user from a channel (operator only) |
| `INVITE <nickname> <channel>` | Invite a user to a channel |
| `TOPIC <channel> [message]` | View or set the channel topic |
| `QUIT [message]` | Disconnect from the server |

## Channel Modes

| Mode | Description |
|------|-------------|
| `i` | Invite-only |
| `k` | Channel key (password) |
| `l` | User limit |
| `o` | Grant/revoke operator privileges |
| `t` | Restrict TOPIC to operators |
