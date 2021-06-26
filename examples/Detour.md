# Detour
## Starting all detours at once
```
void Hook(int p1)
{

	Detour["Example"]->Callback<void>(p1);
}

extern "C" 
{
    int module_start(size_t args, const void* argp)
    {
        SetupDetour(0x0000, (void*)Hook, 14, "Example");
	    StartDetours();

        return SCE_OK;
    }
    
    int module_stop(size_t args, const void* argp)
    {
        DestroyDetours();

        return SCE_OK;
    }   
}
```

## Example for starting detours separately

```
void Hook(int p1)
{

	Detour["Example"]->Callback<void>(p1);
}

extern "C" 
{
    int module_start(size_t args, const void* argp)
    {
        SetupDetour(0x0000, (void*)Hook, 14, "Example");
	    Detour["Example"]->Start();

        return SCE_OK;
    }
    
    int module_stop(size_t args, const void* argp)
    {
        Detour["Example"]->Stop();

        return SCE_OK;
    }   
}
```