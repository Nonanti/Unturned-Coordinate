# Unturned-Coordinate

This plugin shows the player's coordinate.

```
namespace Unturned_Kordinat
{
    public class Main :  RocketPlugin
    {
        public static Main Instance;
     protected override void Load()
     {
            base.Load();
            Instance = this;
            U.Events.OnPlayerConnected += oyuncubaglandı;
        } 
        private void oyuncubaglandı(UnturnedPlayer caller) 
        {
            if ((DateTime.Now - DateTime.Now).TotalSeconds >= 0.1)
            {
                var player = (UnturnedPlayer)caller;
                var x = System.Math.Ceiling(player.Position.x).ToString();
                var y = System.Math.Ceiling(player.Position.y).ToString();
                var z = System.Math.Ceiling(player.Position.z).ToString();
                EffectManager.sendUIEffect(3162, 1, player.CSteamID, true, x, y, z);
            }
        } 
    }
}
```
