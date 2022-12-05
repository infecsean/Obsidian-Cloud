# ShaderLab stuff
---
So ShaderLab structure probably goes like this

Pass tags: [Pass tags in URP](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@11.0/manual/urp-shaders/urp-shaderlab-pass-tags.html#urp-pass-tags-lightmode)


```c#
//not c# just they dont have hlsl/shaderlab syntax highlights
Shader "Folder/Subfolder"
{
	PackageRequirements // i think this can be in any block
	{
	
	}
	Properties
	{
		[attribute] name("inspector display", type) = default value
	}
	SubShader
	{
		LOD value
		Tags { "Tagname" = "tag" "Tagname 2" = "Tag 2"}
		
		HLSLINCLUDE
		
		ENDHLSL
		
		ShaderLab Commands

		Pass
		{
			Name "Somename"
			Tags { "Tagname" = "Value"}
			
			HLSLPROGRAM
			
			ENDHLSL
		
		}


	}
	
	Fallback "Fallback shader name"
}

```