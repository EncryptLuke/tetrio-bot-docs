# `server/environment`

This endpoint provides environment data about the server. Comparable to TETRIO_ENV in [tetrio.js.](https://tetr.io/js/tetrio.js)


To use this endpoint, you do not need any authorization token.

## Format

* (object):
    * (boolean) `success`: Indicates if the request was successful.
    * (object) `stats`: Contains various statistics about the server.
        * (number) `players`: The total number of players.
        * (number) `users`: The total number of users.
        * (number) `gamesplayed`: Total number of games played.
        * (number) `gametime`: Total game time in milliseconds.
    * (object) `signature`: Provides signature and configuration details.
        * (string) `version`: Current game version..
        * (boolean) `countdown`: Countdown configuration.
        * (boolean) `novault`: Indicates if OSK Vault is off.
        * (boolean) `noceriad`: Indicates if the ceriad feature is off.
        * (boolean) `norichpresence`: Indicates if Discord Rich Presence is disabled.
        * (boolean) `noreplaydispute`: Indicates if replay dispute feature is off.
        * (number) `supporter_specialthanks_goal`: Goal amount for special thanks supporters.
        * (number) `xp_multiplier`: Experience points multiplier.
        * (object) `catalog`: Contains pricing details for supporters.
            * (object) `supporter`: Pricing details for supporter subscriptions.
                * (number) `price`: Base price.
                * (number) `price_bulk`: Bulk price.
                * (number) `price_gift`: Gift price.
                * (number) `price_gift_bulk`: Bulk gift price.
                * (number) `bulk_after`: Number of items after which bulk pricing applies.
                * (number) `normal_price`: Base normal price.
                * (number) `normal_price_bulk`: Normal bulk price.
                * (number) `normal_price_gift`: Normal gift price.
                * (number) `normal_price_gift_bulk`: Normal bulk gift price.
                * (number) `normal_bulk_after`: Number of items after which normal bulk pricing applies.
        * (number) `league_mm_roundtime_min`: Minimum TETRA LEAGUE match-making round time in minutes.
        * (number) `league_mm_roundtime_max`: Maximum TETRA LEAGUE match-making round time in minutes.
        * (object) `league_additional_settings`: Additional settings for the league.
        * (object) `league_season`: Current, previous, and next season details for the league.
            * (string) `current`: Current season.
            * (string) `prev`: Previous season.
            * (string) `next`: Next season.
            * (number) `next_at`: Timestamp for the start of next season.
            * (boolean) `ranked`: Indicates if the current season is ranked.
        * (boolean) `zenith_duoisfree`: Indicates if Zenith Duo mode is free. (currently supporter locked)
        * (string) `domain`: Primary domain of the server.
        * (string) `domain_hash`: Hash of the primary domain.
        * (string) `ch_domain`: TETRA CHANNEL Domain.
        * (string) `mode`: Mode of the server.
        * (object) `commit`: Commit details of the server.
            * (string) `id`: Commit ID.
            * (number) `time`: Commit timestamp.
        * (string) `branch`: Branch of the server.
        * (object) `loggings`: Logging configuration.
            * (boolean) `manager`: Indicates if manager logging is enabled.
            * (boolean) `ribbon`: Indicates if ribbon logging is enabled.
        * (string) `serverCycle`: Server cycle identifier.
        * (object) `build`: Build details of the server.
            * (string) `id`: Build ID.
            * (number) `time`: Build timestamp.
    * (string) `vx`: Signature verification string.

