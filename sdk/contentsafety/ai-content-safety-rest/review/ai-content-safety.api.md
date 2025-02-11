## API Report File for "@azure-rest/ai-content-safety"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { Client } from '@azure-rest/core-client';
import { ClientOptions } from '@azure-rest/core-client';
import { ErrorResponse } from '@azure-rest/core-client';
import { HttpResponse } from '@azure-rest/core-client';
import { KeyCredential } from '@azure/core-auth';
import { Paged } from '@azure/core-paging';
import { PagedAsyncIterableIterator } from '@azure/core-paging';
import { PathUncheckedResponse } from '@azure-rest/core-client';
import { RawHttpHeaders } from '@azure/core-rest-pipeline';
import { RequestParameters } from '@azure-rest/core-client';
import { StreamableMethod } from '@azure-rest/core-client';

// @public (undocumented)
export interface AddBlockItems {
    post(options?: AddBlockItemsParameters): StreamableMethod<AddBlockItems200Response | AddBlockItemsDefaultResponse>;
}

// @public
export interface AddBlockItems200Response extends HttpResponse {
    // (undocumented)
    body: AddBlockItemsResultOutput;
    // (undocumented)
    status: "200";
}

// @public (undocumented)
export interface AddBlockItemsBodyParam {
    // (undocumented)
    body?: AddBlockItemsOptions;
}

// @public (undocumented)
export interface AddBlockItemsDefaultHeaders {
    "x-ms-error-code"?: string;
}

// @public (undocumented)
export interface AddBlockItemsDefaultResponse extends HttpResponse {
    // (undocumented)
    body: ErrorResponse;
    // (undocumented)
    headers: RawHttpHeaders & AddBlockItemsDefaultHeaders;
    // (undocumented)
    status: string;
}

// @public
export interface AddBlockItemsOptions {
    blockItems: Array<TextBlockItemInfo>;
}

// @public (undocumented)
export type AddBlockItemsParameters = AddBlockItemsBodyParam & RequestParameters;

// @public
export interface AddBlockItemsResultOutput {
    value?: Array<TextBlockItemOutput>;
}

// @public (undocumented)
export interface AnalyzeImage {
    post(options: AnalyzeImageParameters): StreamableMethod<AnalyzeImage200Response | AnalyzeImageDefaultResponse>;
}

// @public
export interface AnalyzeImage200Response extends HttpResponse {
    // (undocumented)
    body: AnalyzeImageResultOutput;
    // (undocumented)
    status: "200";
}

// @public (undocumented)
export interface AnalyzeImageBodyParam {
    body: AnalyzeImageOptions;
}

// @public (undocumented)
export interface AnalyzeImageDefaultHeaders {
    "x-ms-error-code"?: string;
}

// @public (undocumented)
export interface AnalyzeImageDefaultResponse extends HttpResponse {
    // (undocumented)
    body: ErrorResponse;
    // (undocumented)
    headers: RawHttpHeaders & AnalyzeImageDefaultHeaders;
    // (undocumented)
    status: string;
}

// @public
export interface AnalyzeImageOptions {
    categories?: string[];
    image: ImageData_2;
}

// @public
export interface AnalyzeImageOptionsOutput {
    categories?: string[];
    image: ImageDataOutput;
}

// @public (undocumented)
export type AnalyzeImageParameters = AnalyzeImageBodyParam & RequestParameters;

// @public
export interface AnalyzeImageResultOutput {
    hateResult?: ImageAnalyzeSeverityResultOutput;
    selfHarmResult?: ImageAnalyzeSeverityResultOutput;
    sexualResult?: ImageAnalyzeSeverityResultOutput;
    violenceResult?: ImageAnalyzeSeverityResultOutput;
}

// @public (undocumented)
export interface AnalyzeText {
    post(options: AnalyzeTextParameters): StreamableMethod<AnalyzeText200Response | AnalyzeTextDefaultResponse>;
}

// @public
export interface AnalyzeText200Response extends HttpResponse {
    // (undocumented)
    body: AnalyzeTextResultOutput;
    // (undocumented)
    status: "200";
}

// @public (undocumented)
export interface AnalyzeTextBodyParam {
    body: AnalyzeTextOptions;
}

// @public (undocumented)
export interface AnalyzeTextDefaultHeaders {
    "x-ms-error-code"?: string;
}

// @public (undocumented)
export interface AnalyzeTextDefaultResponse extends HttpResponse {
    // (undocumented)
    body: ErrorResponse;
    // (undocumented)
    headers: RawHttpHeaders & AnalyzeTextDefaultHeaders;
    // (undocumented)
    status: string;
}

// @public
export interface AnalyzeTextOptions {
    blocklistNames?: string[];
    breakByBlocklists?: boolean;
    categories?: string[];
    text: string;
}

// @public
export interface AnalyzeTextOptionsOutput {
    blocklistNames?: string[];
    breakByBlocklists?: boolean;
    categories?: string[];
    text: string;
}

// @public (undocumented)
export type AnalyzeTextParameters = AnalyzeTextBodyParam & RequestParameters;

// @public
export interface AnalyzeTextResultOutput {
    blocklistsMatchResults?: Array<TextBlocklistMatchResultOutput>;
    hateResult?: TextAnalyzeSeverityResultOutput;
    selfHarmResult?: TextAnalyzeSeverityResultOutput;
    sexualResult?: TextAnalyzeSeverityResultOutput;
    violenceResult?: TextAnalyzeSeverityResultOutput;
}

// @public (undocumented)
export type ContentSafetyClient = Client & {
    path: Routes;
};

// @public
function createClient(endpoint: string, credentials: KeyCredential, options?: ClientOptions): ContentSafetyClient;
export default createClient;

// @public
export interface CreateOrUpdateTextBlocklist200Response extends HttpResponse {
    // (undocumented)
    body: TextBlocklistOutput;
    // (undocumented)
    status: "200";
}

// @public
export interface CreateOrUpdateTextBlocklist201Response extends HttpResponse {
    // (undocumented)
    body: TextBlocklistOutput;
    // (undocumented)
    status: "201";
}

// @public (undocumented)
export interface CreateOrUpdateTextBlocklistBodyParam {
    body: TextBlocklistResourceMergeAndPatch;
}

// @public (undocumented)
export interface CreateOrUpdateTextBlocklistDefaultHeaders {
    "x-ms-error-code"?: string;
}

// @public (undocumented)
export interface CreateOrUpdateTextBlocklistDefaultResponse extends HttpResponse {
    // (undocumented)
    body: ErrorResponse;
    // (undocumented)
    headers: RawHttpHeaders & CreateOrUpdateTextBlocklistDefaultHeaders;
    // (undocumented)
    status: string;
}

// @public (undocumented)
export interface CreateOrUpdateTextBlocklistMediaTypesParam {
    contentType: "application/merge-patch+json";
}

// @public (undocumented)
export type CreateOrUpdateTextBlocklistParameters = CreateOrUpdateTextBlocklistMediaTypesParam & CreateOrUpdateTextBlocklistBodyParam & RequestParameters;

// @public
export interface DeleteTextBlocklist204Response extends HttpResponse {
    // (undocumented)
    status: "204";
}

// @public (undocumented)
export interface DeleteTextBlocklistDefaultHeaders {
    "x-ms-error-code"?: string;
}

// @public (undocumented)
export interface DeleteTextBlocklistDefaultResponse extends HttpResponse {
    // (undocumented)
    body: ErrorResponse;
    // (undocumented)
    headers: RawHttpHeaders & DeleteTextBlocklistDefaultHeaders;
    // (undocumented)
    status: string;
}

// @public (undocumented)
export type DeleteTextBlocklistParameters = RequestParameters;

// @public
export type GetArrayType<T> = T extends Array<infer TData> ? TData : never;

// @public
export type GetPage<TPage> = (pageLink: string, maxPageSize?: number) => Promise<{
    page: TPage;
    nextPageLink?: string;
}>;

// @public (undocumented)
export interface GetTextBlocklist {
    delete(options?: DeleteTextBlocklistParameters): StreamableMethod<DeleteTextBlocklist204Response | DeleteTextBlocklistDefaultResponse>;
    get(options?: GetTextBlocklistParameters): StreamableMethod<GetTextBlocklist200Response | GetTextBlocklistDefaultResponse>;
    patch(options: CreateOrUpdateTextBlocklistParameters): StreamableMethod<CreateOrUpdateTextBlocklist200Response | CreateOrUpdateTextBlocklist201Response | CreateOrUpdateTextBlocklistDefaultResponse>;
}

// @public
export interface GetTextBlocklist200Response extends HttpResponse {
    // (undocumented)
    body: TextBlocklistOutput;
    // (undocumented)
    status: "200";
}

// @public (undocumented)
export interface GetTextBlocklistDefaultHeaders {
    "x-ms-error-code"?: string;
}

// @public (undocumented)
export interface GetTextBlocklistDefaultResponse extends HttpResponse {
    // (undocumented)
    body: ErrorResponse;
    // (undocumented)
    headers: RawHttpHeaders & GetTextBlocklistDefaultHeaders;
    // (undocumented)
    status: string;
}

// @public (undocumented)
export interface GetTextBlocklistItem {
    get(options?: GetTextBlocklistItemParameters): StreamableMethod<GetTextBlocklistItem200Response | GetTextBlocklistItemDefaultResponse>;
}

// @public
export interface GetTextBlocklistItem200Response extends HttpResponse {
    // (undocumented)
    body: TextBlockItemOutput;
    // (undocumented)
    status: "200";
}

// @public (undocumented)
export interface GetTextBlocklistItemDefaultHeaders {
    "x-ms-error-code"?: string;
}

// @public (undocumented)
export interface GetTextBlocklistItemDefaultResponse extends HttpResponse {
    // (undocumented)
    body: ErrorResponse;
    // (undocumented)
    headers: RawHttpHeaders & GetTextBlocklistItemDefaultHeaders;
    // (undocumented)
    status: string;
}

// @public (undocumented)
export type GetTextBlocklistItemParameters = RequestParameters;

// @public (undocumented)
export type GetTextBlocklistParameters = RequestParameters;

// @public
export interface ImageAnalyzeSeverityResultOutput {
    category: string;
    severity: number;
}

// @public
interface ImageData_2 {
    blobUrl?: string;
    content?: string;
}
export { ImageData_2 as ImageData }

// @public
export interface ImageDataOutput {
    blobUrl?: string;
    content?: string;
}

// @public (undocumented)
export function isUnexpected(response: AnalyzeText200Response | AnalyzeTextDefaultResponse): response is AnalyzeTextDefaultResponse;

// @public (undocumented)
export function isUnexpected(response: AnalyzeImage200Response | AnalyzeImageDefaultResponse): response is AnalyzeImageDefaultResponse;

// @public (undocumented)
export function isUnexpected(response: GetTextBlocklist200Response | GetTextBlocklistDefaultResponse): response is GetTextBlocklistDefaultResponse;

// @public (undocumented)
export function isUnexpected(response: CreateOrUpdateTextBlocklist200Response | CreateOrUpdateTextBlocklist201Response | CreateOrUpdateTextBlocklistDefaultResponse): response is CreateOrUpdateTextBlocklistDefaultResponse;

// @public (undocumented)
export function isUnexpected(response: DeleteTextBlocklist204Response | DeleteTextBlocklistDefaultResponse): response is DeleteTextBlocklistDefaultResponse;

// @public (undocumented)
export function isUnexpected(response: ListTextBlocklists200Response | ListTextBlocklistsDefaultResponse): response is ListTextBlocklistsDefaultResponse;

// @public (undocumented)
export function isUnexpected(response: AddBlockItems200Response | AddBlockItemsDefaultResponse): response is AddBlockItemsDefaultResponse;

// @public (undocumented)
export function isUnexpected(response: RemoveBlockItems204Response | RemoveBlockItemsDefaultResponse): response is RemoveBlockItemsDefaultResponse;

// @public (undocumented)
export function isUnexpected(response: GetTextBlocklistItem200Response | GetTextBlocklistItemDefaultResponse): response is GetTextBlocklistItemDefaultResponse;

// @public (undocumented)
export function isUnexpected(response: ListTextBlocklistItems200Response | ListTextBlocklistItemsDefaultResponse): response is ListTextBlocklistItemsDefaultResponse;

// @public (undocumented)
export interface ListTextBlocklistItems {
    get(options?: ListTextBlocklistItemsParameters): StreamableMethod<ListTextBlocklistItems200Response | ListTextBlocklistItemsDefaultResponse>;
}

// @public
export interface ListTextBlocklistItems200Response extends HttpResponse {
    // (undocumented)
    body: TextBlockItemListOutput;
    // (undocumented)
    status: "200";
}

// @public (undocumented)
export interface ListTextBlocklistItemsDefaultHeaders {
    "x-ms-error-code"?: string;
}

// @public (undocumented)
export interface ListTextBlocklistItemsDefaultResponse extends HttpResponse {
    // (undocumented)
    body: ErrorResponse;
    // (undocumented)
    headers: RawHttpHeaders & ListTextBlocklistItemsDefaultHeaders;
    // (undocumented)
    status: string;
}

// @public (undocumented)
export type ListTextBlocklistItemsParameters = ListTextBlocklistItemsQueryParam & RequestParameters;

// @public (undocumented)
export interface ListTextBlocklistItemsQueryParam {
    // (undocumented)
    queryParameters?: ListTextBlocklistItemsQueryParamProperties;
}

// @public (undocumented)
export interface ListTextBlocklistItemsQueryParamProperties {
    maxpagesize?: number;
    skip?: number;
    top?: number;
}

// @public (undocumented)
export interface ListTextBlocklists {
    get(options?: ListTextBlocklistsParameters): StreamableMethod<ListTextBlocklists200Response | ListTextBlocklistsDefaultResponse>;
}

// @public
export interface ListTextBlocklists200Response extends HttpResponse {
    // (undocumented)
    body: TextBlocklistListOutput;
    // (undocumented)
    status: "200";
}

// @public (undocumented)
export interface ListTextBlocklistsDefaultHeaders {
    "x-ms-error-code"?: string;
}

// @public (undocumented)
export interface ListTextBlocklistsDefaultResponse extends HttpResponse {
    // (undocumented)
    body: ErrorResponse;
    // (undocumented)
    headers: RawHttpHeaders & ListTextBlocklistsDefaultHeaders;
    // (undocumented)
    status: string;
}

// @public (undocumented)
export type ListTextBlocklistsParameters = RequestParameters;

// @public
export function paginate<TResponse extends PathUncheckedResponse>(client: Client, initialResponse: TResponse, options?: PagingOptions<TResponse>): PagedAsyncIterableIterator<PaginateReturn<TResponse>>;

// @public
export type PaginateReturn<TResult> = TResult extends {
    body: {
        value?: infer TPage;
    };
} ? GetArrayType<TPage> : Array<unknown>;

// @public
export interface PagingOptions<TResponse> {
    customGetPage?: GetPage<PaginateReturn<TResponse>[]>;
}

// @public (undocumented)
export interface RemoveBlockItems {
    post(options?: RemoveBlockItemsParameters): StreamableMethod<RemoveBlockItems204Response | RemoveBlockItemsDefaultResponse>;
}

// @public
export interface RemoveBlockItems204Response extends HttpResponse {
    // (undocumented)
    status: "204";
}

// @public (undocumented)
export interface RemoveBlockItemsBodyParam {
    // (undocumented)
    body?: RemoveBlockItemsOptions;
}

// @public (undocumented)
export interface RemoveBlockItemsDefaultHeaders {
    "x-ms-error-code"?: string;
}

// @public (undocumented)
export interface RemoveBlockItemsDefaultResponse extends HttpResponse {
    // (undocumented)
    body: ErrorResponse;
    // (undocumented)
    headers: RawHttpHeaders & RemoveBlockItemsDefaultHeaders;
    // (undocumented)
    status: string;
}

// @public
export interface RemoveBlockItemsOptions {
    blockItemIds: string[];
}

// @public (undocumented)
export type RemoveBlockItemsParameters = RemoveBlockItemsBodyParam & RequestParameters;

// @public (undocumented)
export interface Routes {
    (path: "/text:analyze"): AnalyzeText;
    (path: "/image:analyze"): AnalyzeImage;
    (path: "/text/blocklists/{blocklistName}", blocklistName: string): GetTextBlocklist;
    (path: "/text/blocklists"): ListTextBlocklists;
    (path: "/text/blocklists/{blocklistName}:addBlockItems", blocklistName: string): AddBlockItems;
    (path: "/text/blocklists/{blocklistName}:removeBlockItems", blocklistName: string): RemoveBlockItems;
    (path: "/text/blocklists/{blocklistName}/blockItems/{blockItemId}", blocklistName: string, blockItemId: string): GetTextBlocklistItem;
    (path: "/text/blocklists/{blocklistName}/blockItems", blocklistName: string): ListTextBlocklistItems;
}

// @public
export interface TextAnalyzeSeverityResultOutput {
    category: string;
    severity: number;
}

// @public
export interface TextBlockItemInfo {
    description?: string;
    text: string;
}

// @public
export type TextBlockItemListOutput = Paged<TextBlockItemOutput>;

// @public
export interface TextBlockItemOutput {
    blockItemId: string;
    description?: string;
    text: string;
}

// @public
export interface TextBlocklist {
    blocklistName: string;
    description?: string;
}

// @public
export type TextBlocklistListOutput = Paged<TextBlocklistOutput>;

// @public
export interface TextBlocklistMatchResultOutput {
    blockItemId: string;
    blockItemText: string;
    blocklistName: string;
    length: number;
    offset: number;
}

// @public
export interface TextBlocklistOutput {
    blocklistName: string;
    description?: string;
}

// @public
export type TextBlocklistResourceMergeAndPatch = Partial<TextBlocklist>;

// (No @packageDocumentation comment for this package)

```
