# Delete Pools

If you no longer need a pool, you can delete it. However, a pool can only be deleted if it doesn't contain any sub-pools. If the pool you want to delete contains subpools, you must first delete all subpools.

Note that to delete a pool, you must have the **Manager** role in the parent of the pool you want to delete.

## Deleting a pool <a href="#pool-deletion" id="pool-deletion"></a>

{% hint style="warning" %}
Once a pool is deleted, it cannot be recovered
{% endhint %}

To delete a pool:

1. Navigate to the **Pools** page.
2. In the **Actions** column, select the delete icon <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGAAAABgCAYAAADimHc4AAAChklEQVR4AeycvVHDQBCFLYogVSMk9EEHDuiFwB24BlISCiAklDOGIsTuDIFItCPu1u9O/hjtIM/69ud9fg4c6O7An1QBAEjlPxwAAACxAuL2OAAAYgXE7XEAAMQKiNvjAACIFRC3v00HiEVftgfAUg3BfXMAxnGcx8QQaLzasjkAq9PuMAkAMVQA9A6g9vd1th6tzYsDsokH9QEQCJSdBkC2wkF9AAQCZaevCCB7lT7rA0DMDQC9A5imaZgWEe2zfG+L91vnj94f5XFApFByHgDJAkflARAplJwHQLLAUXkARAol5wGQLHBUHgCRQoX56HhzAKLf66OFSs9H9WvnmwNQe8HW6wFATAgAABArIG6PAwAgVkDcHgcAQKyAuD0OAECCAh2VxAFiWAAAgFgBcXscAACxAuL2OAAAYgXE7XEAAMQKiNvjgP0AEG/SaXscIAYHAACIFRC3xwEAECsgbo8DACBWQNweBwBArIC4PQ4oBFB6HAClChaeB0ChgKXHAVCqYOF5ABQKWHq8OQDR8yOihUvPR/Vr55sDUHvB1usBQEwIAAAQKyBujwMA8A8FdnQEB4hhZgD4WtspepaDOr82u+VWd7P85qs6gGEYPjZP0cmBIWG36gDmef7sRM/NY2bsVh2AbfVqsder+m7VAdhvMT7keYcEzr+7VV2tOgCfzgZ98v97iqydUgC48DbwYN+Zz37fc/gOvkvWDmkAfODL5fJiCzzY/cnizeLbovXLZ/RZTz6775A5cCoAH9wWeLdP0NHi0eLe4s+zpht87TP6rEef3XfIjA0AMse43doAELMHAADECojb4wAAiBUQt8cBABArIG6PAwAgVkDcHgcEALLTPwAAAP//joBvcQAAAAZJREFUAwDvUAbfFPR8cwAAAABJRU5ErkJggg==" alt="<svg xmlns=&#x22;http://www.w3.org/2000/svg&#x22; height=&#x22;24px&#x22; viewBox=&#x22;0 -960 960 960&#x22; width=&#x22;24px&#x22; fill=&#x22;#1f1f1f&#x22;><path d=&#x22;M280-120q-33 0-56.5-23.5T200-200v-520h-40v-80h200v-40h240v40h200v80h-40v520q0 33-23.5 56.5T680-120H280Zm400-600H280v520h400v-520ZM360-280h80v-360h-80v360Zm160 0h80v-360h-80v360ZM280-720v520-520Z&#x22;/></svg>" data-size="line">.&#x20;
3. In the confirmation dialog, select **I understand and want to delete this pool**.
4. Select **Delete** to confirm.

When the pool is deleted, all resources from that pool are reassigned to its parent pool. Any rules that previously referenced the deleted pool are automatically redirected to the root pool.
