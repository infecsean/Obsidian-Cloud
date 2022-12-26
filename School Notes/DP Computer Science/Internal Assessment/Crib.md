# Ayo show me yo crib
---

### Grass Shader Pseudocode
```
sampler2D LightRampTexture;
sampler2D WindTexture;
float4 GrassColor;
float4 WorldSize;
float4 WindSpeed;
float WaveSpeed;
float WaveAmp;
float HeightCutoff;
float HeightFactor;

TimeSinceLoad as Time;
VertexShader as vert();
FragmentShader as frag();

struct Input
{
	float4 vertexPosition;
	float3 vertexNormal;
}

struct Output
{
	float4 pixelPosition;
	float3 normal;
	float2 textureUVCoordinates;
}

Output vert(Input input)
{
	Output output;
	
	Matrix transformationMatrix = Model*View*Projection matrix;
	output.pixelPosition = transformationMatrix * input.vertexPosition;
	
	Matrix worldMatrix;
	output.normal = normalize(inverseTransform(worldMatrix, input.vertexNormal));
	
	Matrix currentObjectModelMatrix;
	float4 worldPosition = currentObjectModelMatrix * input.vertexPosition;
	float2 samplePosition = worldPosition.xz/WorldSize.xz + Time * WindSpeed.xz;
	float windSample = sample WindTexture at samplePosition;
	
	float heightFactor;
	if input.vertexPosition.y > HeightCutoff
		heightFactor = input.vertexPosition.y;
	else
		heightFactor = 0;
	endif
	
	output.pixelPosition.z += sin(WaveSpeed*windSample) * WaveAmp *HeightFactor;
	output.pixelPosition.x += cos(WaveSpeed*windSample) * WaveAmp *HeightFactor;
	
	return output;
}

float4 frag(Output input) -> TargetObjectColor
{
	float3 worldSpaceLightPosition;
	float3 lightDirection = normalize(worldSpaceLightPosition);
	
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