# `users/me`

This endpoint gets data on the user sending the request.

To use this endpoint, provide a bearer token as authorization. For those unfamiliar with OAuth, that's a header that looks like this:

```http
Authorization: Bearer <token>
```

...where `<token>` is the user's super-duper secret user token. 

## Format

* (object):
    * (boolean) `success`: Whether the request succeeded.
    * (object[]) `errors`?: The resulting errors, if any.
        * (string) `msg`: A single error message.
    * (object) `user`: The user to whom the token belongs.
        * (string) `id`: The ID of the user.
        * (string) `username`:   The username of the user.
        * (string) `country`: The country code of the user.
        * (string) `email`: The email of the user.
        * ([Role](Data/Role.md)) `role`: The role of the user.
        * (string) `ts`: User creation timestamp.
        * (array) `badges`: An array of user badges.
        * (number) `xp`: User XP.
        * (boolean) `privacy_showwon`: Show won games.
        * (boolean) `privacy_showplayed`: Show played games.
        * (boolean) `privacy_showgametime`: Show game time.
        * (boolean) `privacy_showcountry`: Show country.
        * (string) `privacy_privatemode`: Refers to the "WHO CAN ADD ME AS FRIEND" setting.
        * (string) `privacy_status_shallow`: Refers to the "WHO CAN SEE WHETHER I'M ONLINE" setting.
        * (string) `privacy_status_deep`: Refers to the "WHO CAN SEE WHAT I'M DOING" setting.
        * (string) `privacy_status_exact`: Refers to the "WHO CAN SEE WHAT ROOM I'M IN" setting.
        * (string) `privacy_dm`: Refers to the "WHO CAN SEND ME DIRECT MESSAGES" setting.
        * (string) `privacy_invite`: Refers to the "WHO CAN SEND ME INVITES TO ROOMS" setting.
        * (boolean) `thanked`: Whether the user has been thanked for reporting.
        * (array) `banlist`: List of bans/restrictions for user.
        * (array) `warnings`: List of warnings.
        * (string) `bannedstatus`: Ban status.
        * (boolean) `supporter`: Whether the user is a supporter.
            - (number) `supporter_expires`: Timestamp for when supporter status expires.
    - (number) `total_supported`: Total support provided by the user.
    - (object) `league`: Contains league-specific details, left undocumented and set to defaults/immutable for bots.
        - (number) `gamesplayed`
        - (number) `gameswon`
        - (number) `rating`
        - (number) `glicko`
        - (number) `rd`
        - (string) `rank`
        - (number) `apm`
        - (number) `pps`
        - (number) `vs`
        - (boolean) `decaying`
        - (number) `standing`
        - (number) `standing_local`
    - (object) `zenith`
        - (number) `gamesplayed`
        - (number) `floor`
        - (number) `altitude`
        - (unknown/null) `pbish`
        - (unknown/null) `pbishex`
        - (object) `speedrun`
            - (boolean) `seen`
            - (object) `splits`
            - (array) `pb`
            - (array) `gold`
    - (number) `avatar_revision`
    - (object) `totp`
      - (boolean) `enabled`
      - (number) `codes_remaining`
    - (object) `connections`
