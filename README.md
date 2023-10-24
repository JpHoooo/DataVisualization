# 数据图表可视化

将数据以图表的形式显示出来

## Usage

```csharp
using UnityEngine;
using Jphoooo.DataVisualization;
public class Tester : MonoBehaviour
{
    private GraphDrawer drawer ;
    float data;

    private void Start() {

        GraphConfig config = new GraphConfig()
        {
            MaxVisiableCount = 20,
            graphScaleMultiplier = 1f,
            dotSizeMultiplier = 1.2f,
            alignment = Alignment.MiddleCenter,
            YMinMax = new Vector2(2,-2)           
        };
        // or
        GraphConfig config = new GraphConfig();
        drawer =new GraphDrawer(config);
        FunctionPeriodic(InputData, 0.1f);
    }

    void InputData()
    {
        data += Mathf.Deg2Rad * 20;
        drawer.AddData(Mathf.Sin(data));
    }
}
```

---

## Preview

![Graph](https://github.com/JpHoooo/DataVisualization/assets/42137140/725b7887-081d-415f-9813-652c8adf6664)
