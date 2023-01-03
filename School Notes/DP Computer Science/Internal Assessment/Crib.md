# Ayo get in my crib
---

### Grass Shader Pseudocode
```
Texture LightRampTexture;
Texture WindTexture;
float4 GrassColor;
float4 WorldSize;
float4 WindSpeed;
float WaveSpeed;
float HeightCutoff;
float HeightFactor;

struct Input
{
	float4 vertexPosition;
	float3 vertexNormal;
}

struct Output
{
	float4 pixelPosition;
	float3 normal;
}

Output vertexShader(Input input)
{
	Output output;
	Matrix transformationMatrix = Model*View*Projection matrix;
	output.pixelPosition = transformationMatrix * input.vertexPosition;
	Matrix worldMatrix;
	output.normal = normalize(inverseTransform(worldMatrix, input.vertexNormal));
	Matrix currentObjectModelMatrix;
	float4 worldPosition = currentObjectModelMatrix * input.vertexPosition;
	float2 samplePosition = worldPosition.xz/WorldSize.xz + TimeSinceLoaded * WindSpeed.xz;
	float windSample = sample WindTexture at samplePosition;
	float heightFactor;
	if input.vertexPosition.y > HeightCutoff
		heightFactor = input.vertexPosition.y;
	else
		heightFactor = 0;
	endif
	
	output.pixelPosition.z += sin(WaveSpeed*windSample)*heightFactor;
	output.pixelPosition.x += cos(WaveSpeed*windSample)*heightFactor;
	return output;
}

float4 fragmentShader(Output input) -> TargetObjectColor
{
	float3 LightPosition;
	float3 lightDirection = normalize(LightPosition);
	float dot = dot product of input.normal and lightDirection;
	float min = 0.001;
	float max = 1.0;
	float ramp = clamp dot between min & max;
	float4 lighting = Look up texture RampTexture at coordinates (ramp, 0.5);
	float4 ambientLight;
	float4 output = lighting * GrassColor * ambientLight;
	return output;
}

```

