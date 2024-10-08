## API Report File for "@tldraw/sync"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { Editor } from 'tldraw';
import { Signal } from 'tldraw';
import { TLAssetStore } from 'tldraw';
import { TLStoreSchemaOptions } from 'tldraw';
import { TLStoreWithStatus } from 'tldraw';

// @public (undocumented)
export type RemoteTLStoreWithStatus = Exclude<TLStoreWithStatus, {
    status: 'not-synced';
} | {
    status: 'synced-local';
}>;

// @public
export interface TLSyncUserInfo {
    color?: null | string;
    id: string;
    name?: null | string;
}

// @public
export function useSync(opts: UseSyncOptions & TLStoreSchemaOptions): RemoteTLStoreWithStatus;

// @public
export function useSyncDemo(options: UseSyncDemoOptions & TLStoreSchemaOptions): RemoteTLStoreWithStatus;

// @public (undocumented)
export interface UseSyncDemoOptions {
    // @internal (undocumented)
    host?: string;
    roomId: string;
    userInfo?: Signal<TLSyncUserInfo> | TLSyncUserInfo;
}

// @public
export interface UseSyncOptions {
    assets: TLAssetStore;
    // @internal (undocumented)
    onMount?(editor: Editor): void;
    // @internal
    roomId?: string;
    // @internal (undocumented)
    trackAnalyticsEvent?(name: string, data: {
        [key: string]: any;
    }): void;
    uri: (() => Promise<string> | string) | string;
    userInfo?: Signal<TLSyncUserInfo> | TLSyncUserInfo;
}


export * from "@tldraw/sync-core";

// (No @packageDocumentation comment for this package)

```
