AddEventHandler('playerConnecting', function(playerName --[[ string ]], setKickReason --[[ function(string) ]], deferrals --[[ table ]]) end)

AddEventHandler('playerDropped', function()
    RconLog({ msgType = 'playerDropped', netID = source, name = GetPlayerName(source) })

    names[source] = nil
end)

AddEventHandler('rconCommand', function(commandName, args)
    if commandName:lower() == 'clientkick' then
        local playerId = table.remove(args, 1)
        local msg = table.concat(args, ' ')

        DropPlayer(playerId, msg)

        CancelEvent()
    end
end)

exports.spawnmanager:addSpawnPoint({
    x = -802.311,
    y = 175.056,
    z = 72.8446,
    heading = 180.0,
    model = "a_m_y_hipster_01"
})
