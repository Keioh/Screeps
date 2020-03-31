var worker = {
    run: function(creep)
    {
        var sources = creep.room.find(FIND_SOURCES);
        
        if(creep.store.getFreeCapacity() == 0)
        {
            creep.moveTo(Game.spawns['MainSpawn']);
            creep.transfer(Game.spawns['MainSpawn'], RESOURCE_ENERGY);
        }
        else
        { 
            if(sources == null)
            {
                var all_exit = creep.room.find(FIND_EXIT);
        
                creep.moveTo(all_exit[0]);
            }
            else
            { 
                creep.moveTo(sources[0]);
                creep.harvest(sources[0]);
            }
        }
    }
}

module.exports = worker;