
Create a fiver acount of build websits






Create a fiver acount of build websits
import { generateStaticParamsFor, importPage } from 'nextra/pages'
import { useMDXComponents } from '../../../mdx-components'

type Params = {
  params: {
    mdxPath: string
  }
}

export const generateStaticParams = generateStaticParamsFor('mdxPath')

export async function generateMetadata({ params }: Params) {
  const { metadata } = await importPage(params.mdxPath)
  return metadata
}

const Wrapper = useMDXComponents().wrapper

export default async function Page({ params }: Params) {
  const result = await importPage(params.mdxPath)
  const { default: MDXContent, toc, metadata } = result

  return (
    <Wrapper toc={toc} metadata={metadata}>
      <MDXContent params={params} />
    </Wrapper>
  )

























Create a fiver acount of build websits
import { generateStaticParamsFor, importPage } from 'nextra/pages'
import { useMDXComponents } from '../../../mdx-components'

type Params = {
  params: {
    mdxPath: string
  }
}

export const generateStaticParams = generateStaticParamsFor('mdxPath')

export async function generateMetadata({ params }: Params) {
  const { metadata } = await importPage(params.mdxPath)
  return metadata
}

const Wrapper = useMDXComponents().wrapper

export default async function Page({ params }: Params) {
  const result = await importPage(params.mdxPath)
  const { default: MDXContent, toc, metadata } = result

  return (
    <Wrapper toc={toc} metadata={metadata}>
      <MDXContent params={params} />
    </Wrapper>
  )
}
